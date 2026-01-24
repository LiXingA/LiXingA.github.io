<!--{"pinCode":true,"dname":"ef67ee11-9454-48ee-bbd4-3a66c87dda14","codeMode":"js"}-->
```js
555666777888
```

<!--{"pinCode":false,"dname":"63171d52-a477-4b67-b230-8a9a72227af9","codeMode":"markdown"}-->
# Shader

This notebook provides a little helper for fragment shaders. It is heavily inspired by Inigo Quilez’s [Shadertoy](https://www.shadertoy.com). To import into your notebook:

~~~js
import {shader} from "@mbostock/shader"
~~~

For example:

<!--{"pinCode":false,"dname":"c435921f-ab59-447e-acdf-80ca0734ef94","codeMode":"js"}-->
```js
shader({width: 640, height: 100})`
void mainImage(out vec4 fragColor, in vec2 fragCoord) {
  fragColor = vec4(vec2(fragCoord.xy / iResolution.xy), 0.0, 1.0);
}`
```

<!--{"pinCode":false,"dname":"01832760-6519-4304-85b1-a68363899532","codeMode":"js"}-->
```js
shader({width: 640, height: 100})`
const float size = 25.0;

void mainImage(out vec4 fragColor, in vec2 fragCoord) {
  vec2 p = fragCoord.xy;
  float k = float(mod(p.x, size * 2.0) < size == mod(p.y, size * 2.0) < size);
  fragColor = vec4(vec3(k), 1.0);
}`
```

<!--{"pinCode":false,"dname":"8bce9da6-a9a1-44ec-a0fd-0db8b0a55886","codeMode":"markdown"}-->
If *width* is not specified, it defaults to 640. If *height* is not specified, it defaults to 480. A *devicePixelRatio* option may also be specified; it defaults to the native value. Shaders can reference the const vec3 iResolution for the canvas dimensions; *z* stores the devicePixelRatio.

<!--{"pinCode":false,"dname":"9471ee1c-0169-4f48-a57e-64060565cb2e","codeMode":"markdown"}-->
The *iTime* option enables time-dependent shaders with the same behavior as on Shadertoy: it defines a uniform float iTime whose value is in seconds. (iMouse and others are not yet implemented; maybe in the future.) If you also pass in the *visibility* option using Observable’s built-in [visibility function](/@observablehq/awaiting-visibility), Shader will only render when the canvas is visible.

<!--{"pinCode":false,"dname":"b0ab7d47-4df4-4f90-a710-04b05609ee3b","codeMode":"js"}-->
```js
shader({height: 100, iTime: true, visibility})`
const float size = 25.0;

mat2 rotate2d(float a) {
  return mat2(cos(a), -sin(a), sin(a), cos(a));
}

void mainImage(out vec4 fragColor, in vec2 fragCoord) {
  vec2 p = (fragCoord.xy - iResolution.xy / 2.0) * rotate2d(iTime / 10.0);
  float k = float(mod(p.x, size * 2.0) < size == mod(p.y, size * 2.0) < size);
  fragColor = vec4(vec3(k), 1.0);
}`
```

<!--{"pinCode":false,"dname":"f72b5d09-d9e6-4da2-a87a-1d1a931e1c36","codeMode":"markdown"}-->
More generally, the *uniforms* option allows you to declare uniforms. These can then by updated programmatically by calling *canvas*.update. Currently only float uniforms are supported.

<!--{"pinCode":false,"dname":"c74072da-4f33-413e-9ea4-a6ad09e6f47a","codeMode":"js"}-->
```js
canvas = (shader({height: 100, uniforms: {angle: "float"}})`
const float size = 25.0;

mat2 rotate2d(float a) {
  return mat2(cos(a), -sin(a), sin(a), cos(a));
}

void mainImage(out vec4 fragColor, in vec2 fragCoord) {
  vec2 p = (fragCoord.xy - iResolution.xy / 2.0) * rotate2d(angle);
  float k = float(mod(p.x, size * 2.0) < size == mod(p.y, size * 2.0) < size);
  fragColor = vec4(vec3(k), 1.0);
}`)
```

<!--{"pinCode":false,"dname":"6ea5df33-183a-4958-9fb4-38d06571101a","codeMode":"js"}-->
```js
canvas.update({angle: now / 10000.0 % (2 * Math.PI)})
```

<!--{"pinCode":false,"dname":"c5c12bf6-140b-401d-b734-4a97d548620e","codeMode":"markdown"}-->
If you pass an *inputs* object, the shader can reference uniforms whose value corresponds to the input’s value. If a corresponding uniform is not declared, it is assumed to be a float.

<!--{"pinCode":false,"dname":"b2656606-39de-4d5c-8e2a-d8e77c85d925","codeMode":"js"}-->
```js
viewof angle = (Inputs.range([-Math.PI, Math.PI], {label: "angle"}))
```

<!--{"pinCode":false,"dname":"bb6a5d20-ba3f-47fe-9300-7db156ff9991","codeMode":"js"}-->
```js
viewof size = (Inputs.range([10, 100], {value: 25, transform: Math.log, label: "size"}))
```

<!--{"pinCode":false,"dname":"38def4fb-93d8-4fe4-bce0-6b6fe2afa104","codeMode":"js"}-->
```js
shader({height: 100, inputs: {angle: viewof angle, size: viewof size}})`

mat2 rotate2d(float a) {
  return mat2(cos(a), -sin(a), sin(a), cos(a));
}

void mainImage(out vec4 fragColor, in vec2 fragCoord) {
  vec2 p = (fragCoord.xy - iResolution.xy / 2.0) * rotate2d(angle);
  float k = float(mod(p.x, size * 2.0) < size == mod(p.y, size * 2.0) < size);
  fragColor = vec4(vec3(k), 1.0);
}`
```

<!--{"pinCode":false,"dname":"584aebbc-59c6-43f3-a48b-9370821588dd","codeMode":"markdown"}-->
---

## Implementation

<!--{"pinCode":false,"dname":"9d296820-532b-4633-a9d0-795a2b15bbeb","codeMode":"js"}-->
```js
shader = (function shader({
  width = 640,
  height = 480,
  devicePixelRatio = window.devicePixelRatio,
  invalidation, // when the canvas is considered disposed
  visibility, // if present, only draw when resolves
  uniforms = {}, // declare your uniforms here
  inputs = {}, // bind inputs to uniforms
  iMouse = false, // not yet supported!
  iTime = false, // enable built-in iTime uniform
  sources = [], // extra sources (lib functions etc.)
  preserveDrawingBuffer = false // if you want “Download PNG” to work
} = {}) {
  uniforms = new Map(Object.entries(uniforms).map(([name, type]) => [name, {type}]));
  inputs = new Map(Object.entries(inputs));
  for (const {type} of uniforms.values()) if (type !== "float") throw new Error(`unknown type: ${type}`);
  for (const name of inputs.keys()) if (!uniforms.has(name)) uniforms.set(name, {type: "float"});
  if (iTime && !uniforms.has("iTime")) uniforms.set("iTime", {type: "float"});
  if (visibility !== undefined && typeof visibility !== "function") throw new Error("invalid visibility");
  return function() {
    const source = String.raw.apply(String, arguments);
    const canvas = document.createElement("canvas");
    canvas.width = width * devicePixelRatio;
    canvas.height = height * devicePixelRatio;
    canvas.style = `max-width: 100%; width: ${width}px; height: auto;`;
    const gl = canvas.getContext("webgl", {preserveDrawingBuffer});
    const fragmentShader = createShader(gl, gl.FRAGMENT_SHADER, `precision highp float;
${Array.from(uniforms, ([name, {type}]) => `uniform ${type} ${name};`).join("\n")}
const vec3 iResolution = vec3(
  ${(width * devicePixelRatio).toFixed(1)}, 
  ${(height * devicePixelRatio).toFixed(1)}, 
  ${(devicePixelRatio).toFixed(1)}
);
`, ...sources, source, `
void main() {
  mainImage(gl_FragColor, gl_FragCoord.xy);
}
`);
    const vertexShader = createShader(gl, gl.VERTEX_SHADER, `
attribute vec2 a_vertex;

void main() {
  gl_Position = vec4(a_vertex, 0.0, 1.0);
}
`);
    const vertexBuffer = gl.createBuffer();
    gl.bindBuffer(gl.ARRAY_BUFFER, vertexBuffer);
    gl.bufferData(gl.ARRAY_BUFFER, Float32Array.of(-1, -1, +1, -1, +1, +1, -1, +1), gl.STATIC_DRAW);
    const program = createProgram(gl, vertexShader, fragmentShader);
    gl.useProgram(program);
    gl.bindBuffer(gl.ARRAY_BUFFER, vertexBuffer);
    const a_vertex = gl.getAttribLocation(program, "a_vertex");
    gl.enableVertexAttribArray(a_vertex);
    gl.vertexAttribPointer(a_vertex, 2, gl.FLOAT, false, 0, 0);
    for (const [name, u] of uniforms) u.location = gl.getUniformLocation(program, name);
    const ondispose = invalidation === undefined ? Inputs.disposal(canvas) : invalidation;
    let frame;
    let disposed = false;
    ondispose.then(() => disposed = true);
    async function render() {
      if (visibility !== undefined) await visibility();
      frame = undefined;
      gl.drawArrays(gl.TRIANGLE_FAN, 0, 4);
    }
    Object.assign(canvas, {
      update(values = {}) {
        if (disposed) return false;
        for (const name in values) {
          const u = uniforms.get(name);
          if (!u) throw new Error(`unknown uniform: ${name}`);
          gl.uniform1f(u.location, values[name]);
        }
        frame || requestAnimationFrame(render);
        return true;
      }
    });
    for (const [name, input] of inputs) {
      const u = uniforms.get(name);
      if (!u) throw new Error(`unknown uniform: ${name}`);
      gl.uniform1f(u.location, input.value);
      const update = () => {
        gl.uniform1f(u.location, input.value);
        frame || requestAnimationFrame(render);
      };
      input.addEventListener("input", update);
      ondispose.then(() => input.removeEventListener("input", update));
    }
    if (iTime) {
      frame = true; // always rendering
      const u_time = gl.getUniformLocation(program, "iTime");
      let timeframe;
      (async function tick() {
        if (visibility !== undefined) await visibility();
        gl.uniform1f(u_time, performance.now() / 1000);
        gl.drawArrays(gl.TRIANGLE_FAN, 0, 4);
        return timeframe = requestAnimationFrame(tick);
      })();
      ondispose.then(() => cancelAnimationFrame(timeframe));
    } else {
      gl.drawArrays(gl.TRIANGLE_FAN, 0, 4);
    }
    return canvas;
  };
})
```

<!--{"pinCode":false,"dname":"a6d5fcd3-b66c-4d53-a9d9-41dd3f4957d8","codeMode":"js"}-->
```js
createShader = (function createShader(gl, type, ...sources) {
  const shader = gl.createShader(type);
  gl.shaderSource(shader, sources.join("\n"));
  gl.compileShader(shader);
  if (gl.getShaderParameter(shader, gl.COMPILE_STATUS)) return shader;
  throw new Error(gl.getShaderInfoLog(shader));
})
```

<!--{"pinCode":false,"dname":"eba3783a-f3c4-4a1d-ad5e-97e977d90900","codeMode":"js"}-->
```js
createProgram = (function createProgram(gl, ...shaders) {
  const program = gl.createProgram();
  for (const shader of shaders) gl.attachShader(program, shader);
  gl.linkProgram(program);
  if (gl.getProgramParameter(program, gl.LINK_STATUS)) return program;
  throw new Error(gl.getProgramInfoLog(program));
})
```
