<!--{"pinCode":false,"dname":"51c13e5e-b96b-4212-ad59-b6c9e07332ed","codeMode":"markdown"}-->
```md
***
```

<!--{"pinCode":false,"dname":"3e4d9409-54af-466e-a0fe-d14b84cc9295","codeMode":"markdown"}-->
```md
name: grovebook
description: Create and work with grovebook files - markdown files with interactive cells that can return JavaScript values, HTML, markdown, ObservableHQ Inputs components, or Grove extended library components.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
```

<!--{"pinCode":false,"dname":"df777873-f055-48b7-a066-0415c955a344","codeMode":"markdown"}-->
```md
# Grovebook
```

<!--{"pinCode":false,"dname":"a76306f4-c7e6-4c2e-aff8-bb8b964f1623","codeMode":"markdown"}-->
```md
## When to use this skill
```

<!--{"pinCode":false,"dname":"9e8795e8-2422-447e-be66-ed365260afaf","codeMode":"markdown"}-->
```md
Use this skill when the user wants to:
```

<!--{"pinCode":false,"dname":"77a7ef5e-353e-41fe-b48a-efedba337118","codeMode":"markdown"}-->
```md
* Create or edit grovebook files
* Understand the structure and syntax of grovebooks
* Work with grovebook cells and their metadata
* Generate grovebook content with cells, markdown, and interactive components
```

<!--{"pinCode":false,"dname":"f9a82591-76e2-42d1-8ae9-d030a939a2cc","codeMode":"markdown"}-->
```md
## Overview
```

<!--{"pinCode":false,"dname":"06167825-5e81-4599-963f-493d9160afa2","codeMode":"markdown"}-->
```md
A grovebook file is a markdown file that contains interactive cells. These cells can execute JavaScript code and return various types of content including primitive values, HTML, markdown, ObservableHQ Inputs components, or Grove extended library components.
```

<!--{"pinCode":false,"dname":"61a2f1cc-46ca-4b26-9b3c-78d6986cd2b4","codeMode":"markdown"}-->
```md
## File Extension
```

<!--{"pinCode":false,"dname":"2f3ff289-51ed-4736-b0fd-edd03cf2fe9f","codeMode":"markdown"}-->
```md
Grovebooks MUST end with the .md extension.
```

<!--{"pinCode":false,"dname":"d011e963-045e-49b9-89c7-f373599db907","codeMode":"markdown"}-->
```md
## Cells
```

<!--{"pinCode":false,"dname":"08f87e64-1b82-44ad-8382-5d5cbaf7ad9c","codeMode":"markdown"}-->
```md
A cell looks like:
```

````
<!--{"pinCode":false,"dname":"js-cell","codeMode":"js","hide":false}-->
```js
{
  return 1 + 1;
}
```
````

<!--{"pinCode":false,"dname":"a25e5e92-ce59-4e28-a55d-ccb709208c9c","codeMode":"markdown"}-->
```md
### Schema of a cell
```

<!--{"pinCode":false,"dname":"a12ffba8-b818-4e21-a1b3-6af026e99741","codeMode":"markdown"}-->
```md
1. HTML comment with JSON metadata
2. Code fence with the code for the cell
```

<!--{"pinCode":false,"dname":"adeefca4-a624-4360-bf00-5c1c8ff28f11","codeMode":"markdown"}-->
```md
### Cell metadata
```

<!--{"pinCode":false,"dname":"b11204bf-2c1f-4477-99ae-9a6bd6d9a40e","codeMode":"markdown"}-->
```md
The metadata is a JSON object contained in an HTML comment that precedes the code fence for the cell. It contains the following properties:
```

<!--{"pinCode":false,"dname":"70fe1c55-eadf-498f-b281-894b5140d757","codeMode":"markdown"}-->
```md
* `pinCode`: boolean, whether to pin the cell. If true, the code will display in Grove.
* `dname`: string, unique identifier of the cell.
* `codeMode`: string, the code mode of the cell. Typical values are `js`, `jsx`, and `md`.
* `hide`: boolean, whether to hide the cell while not editing.
```

<!--{"pinCode":false,"dname":"6ae5cecb-1c60-434a-839c-9bf14c3b2b56","codeMode":"markdown"}-->
```md
Example:
```

```
<!--{"pinCode":false,"dname":"js-cell","codeMode":"js","hide":false}-->
```

<!--{"pinCode":false,"dname":"5ae6eb43-f9c2-44aa-9eef-b2a712a225dd","codeMode":"markdown"}-->
```md
### Types of cells
```

<!--{"pinCode":false,"dname":"55420849-2e9e-4e03-baf0-c424b268db1f","codeMode":"markdown"}-->
```md
#### Renderable content
```

<!--{"pinCode":false,"dname":"f14b9c2e-5008-4945-8192-99f6873a8d0d","codeMode":"markdown"}-->
```md
##### HTML
```

````
<!--{"pinCode":false,"dname":"html-cell","codeMode":"js","hide":false}-->
```js
{
  return html`${1 + 1}`;
}
```
````

<!--{"pinCode":false,"dname":"5a2a6a59-2196-48f9-8454-e4532fdd779b","codeMode":"markdown"}-->
```md
##### Markdown with the `md` literal like `{ return md\`\` }\`
```

````
<!--{"pinCode":false,"dname":"markdown-cell","codeMode":"js","hide":false}-->
```js
{
  return md`# Hello, world`;
}
```
````

<!--{"pinCode":false,"dname":"b1e331f5-62f1-4b91-970f-96d16cf2f430","codeMode":"markdown"}-->
```md
##### ObservableHQ's Inputs library
```

<!--{"pinCode":false,"dname":"b1646dc8-1bf8-4a61-92d2-5a3c944052d1","codeMode":"markdown"}-->
```md
See `references/observablehq-inputs.md` for more information about the ObservableHQ Inputs library. One of the following:
```

<!--{"pinCode":true,"dname":"3f8e0147-7a03-459c-acaa-71ff01f57bca","codeMode":"javascript"}-->
```javascript
Inputs.button(content, options)      // Click trigger
Inputs.toggle(options)               // On/off switch
Inputs.checkbox(data, options)       // Multiple selection
Inputs.radio(data, options)          // Single selection (visible)
Inputs.range(extent, options)        // Number slider
Inputs.number(extent?, options)      // Number input only
Inputs.select(data, options)         // Dropdown menu
Inputs.text(options)                 // Single-line text
Inputs.email(options)                // Email input
Inputs.tel(options)                  // Telephone input
Inputs.url(options)                  // URL input
Inputs.password(options)             // Password input
Inputs.textarea(options)             // Multi-line text
Inputs.date(options)                 // Date picker
Inputs.datetime(options)             // Date + time picker
Inputs.color(options)                // Color picker
Inputs.file(options)                 // File upload
```

````
<!--{"pinCode":false,"dname":"my-cell","codeMode":"js","hide":false}-->
```js
viewof name = Inputs.text({label: "Name", placeholder: "What's your name?"});
```
````

<!--{"pinCode":false,"dname":"d2c23712-b18c-442f-a92c-47c17af5bcae","codeMode":"markdown"}-->
```md
##### JSX
```

<!--{"pinCode":false,"dname":"870fa503-eed5-4b3c-b358-dd76e226b5bb","codeMode":"markdown"}-->
```md
###### A custom React component
```

<!--{"pinCode":false,"dname":"48eec819-3dc1-4579-bc6d-75510fe0c4fc","codeMode":"markdown"}-->
```md
* Note that the code mode must be `jsx` for custom React components.
* One component per cell.
* Component definitions and calls to react() must be in separate cells.
```

````
<!--{"pinCode":false,"dname":"jsx-cell","codeMode":"jsx","hide":false}-->
```jsx
function CounterComponent() {
  const [x, setX] = React.useState(0);
  return <button onClick={() => {
    setX(x + 1);
  }}>{x}</button> 
}
```

<!--{"pinCode":false,"dname":"render-react-cell","codeMode":"jsx","hide":false}-->
```jsx
react(<CounterComponent />);
```
````

<!--{"pinCode":false,"dname":"f671ac05-f0b4-44e1-825c-a4101495ada8","codeMode":"markdown"}-->
```md
###### Using AntD
```

<!--{"pinCode":false,"dname":"1a035b9b-1592-4688-8246-0f519d439027","codeMode":"markdown"}-->
```md
* See `references/examples/antd-grovebook-example.md` for an example of using AntD in a grovebook.
* Grove provides AntD 4.16.13.
* One component per cell.
* Component definitions and calls to react() must be in separate cells.
```

````
<!--{"pinCode":false,"dname":"antd-cell","codeMode":"jsx","hide":false}-->
```jsx
function CounterComponent() {
  const {Button} = Antd;
  const [x, setX] = React.useState(0);
  return <Button onClick={() => {
    setX(x + 1);
  }}>{x}</Button> 
}
```

<!--{"pinCode":false,"dname":"render-antd-cell","codeMode":"jsx","hide":false}-->
```jsx
react(<CounterComponent />);
```
````

<!--{"pinCode":false,"dname":"46452292-1e00-4918-a766-cbf0485f6086","codeMode":"markdown"}-->
```md
#### Reactive variable
```

<!--{"pinCode":false,"dname":"ba2bdd27-98f8-4097-9d7a-10f130401099","codeMode":"markdown"}-->
```md
##### Simple reactive variable
```

````
<!--{"pinCode":false,"dname":"reactive-variable-cell1","codeMode":"js","hide":false}-->
```js
x = {
  return 1 + 1;
}
```

<!--{"pinCode":false,"dname":"reactive-variable-cell2","codeMode":"js","hide":false}-->
```js
y = {
  return x + 2;
}
```
````

<!--{"pinCode":false,"dname":"76d7c4b9-5702-4991-bfcf-e9b9970332b2","codeMode":"markdown"}-->
```md
##### viewof
```

<!--{"pinCode":false,"dname":"d439fca1-b083-4aeb-b3b0-027f156dfde4","codeMode":"markdown"}-->
```md
A `viewof` cell creates a link between a user interface element and its value by defining two variables in the DAG: one for the HTML input itself and one for its live data. When a user interacts with the input, the value variable updates automatically, triggering a reactive update of all downstream cells.
```

````
<!--{"pinCode":false,"dname":"viewof-example","codeMode":"js","hide":false}-->
```js
viewof size = Inputs.range([0, 100], {label: "Size"})
```

<!--{"pinCode":false,"dname":"area-cell","codeMode":"js","hide":false}-->
```js
// Automatically re-runs whenever the slider moves
area = Math.PI * (size ** 2)
```
````

<!--{"pinCode":false,"dname":"1a9132ed-ec85-4a0d-8674-6c0bcbd4c03e","codeMode":"markdown"}-->
```md
## GraphXR API
```

<!--{"pinCode":false,"dname":"0000faf5-0ba5-47ad-bda1-e16302674800","codeMode":"markdown"}-->
```md
Grovebooks use GraphXR API to interact with the GraphXR platform.
```

<!--{"pinCode":false,"dname":"7b9d792f-f2c4-47c3-8d57-5307e2227893","codeMode":"markdown"}-->
```md
Visit https://graphxr.dev/docs/graphxr-api/reference for a detailed reference of the GraphXR API.
```

<!--{"pinCode":false,"dname":"44ac258e-fe71-4eb2-a8f8-61b5b9240abd","codeMode":"markdown"}-->
```md
## Grove Library
```

<!--{"pinCode":false,"dname":"88249853-bc50-4ee6-a671-09c590169709","codeMode":"markdown"}-->
```md
Grove includes a rich library of built-in variables and components.
```

<!--{"pinCode":false,"dname":"35d00c9a-16ff-4713-bbde-f0fea62ede7b","codeMode":"markdown"}-->
```md
### Built-in variables
```

<!--{"pinCode":false,"dname":"7cbdad7f-05cb-4eeb-8c9e-ebfdd9cb02ce","codeMode":"markdown"}-->
```md
* `width`: number, the width of the current cell in pixels.
* `selectedNodes`: IterableNodes (GraphXR API type), a reactive variable for the nodes that are currently selected in the graph.
* `selectedEdges`: IterableEdges (GraphXR API type), a reactive variable for the edges that are currently selected in the graph.
* `graph`: GraphSelection (GraphXR API type), a reactive variable for the canvas graph.
* `now`: number, a reactive variable for the current time in milliseconds. Imported from `@observablehq/stdlib/src/now.js`
* `uuidv4`: fucntion, UUID v4 generator (uuid ^8.3.2). e.g. `uuidv4()`
```

<!--{"pinCode":false,"dname":"1cbb2cfc-10a1-4a1c-bf67-bf5e6fef3b20","codeMode":"markdown"}-->
```md
### Visualization libraries
```

<!--{"pinCode":false,"dname":"633d7732-0a7f-4ead-8e5e-aa6ff9c98f6d","codeMode":"markdown"}-->
```md
* `Plot`: Observable Plot v0.6.14
* `d3`: D3.js v7.8.5 (includes d3-hexbin v0.2.2)
* `L`: Leaflet v1.9.3
* `mermaid`: Mermaid v9.2.2
* `dot`: Graphviz (@observablehq/graphviz v0.2.1)
* `svg`: SVG utilities (from @observablehq/stdlib v3.4.1)
* `vl`: Vega-Lite v5.6.0 (uses Vega v5.22.1, vega-lite-api v5.0.0)
```

<!--{"pinCode":false,"dname":"06b24a11-f4bb-4731-aa42-7475b5d98072","codeMode":"markdown"}-->
```md
### Utilities
```

<!--{"pinCode":false,"dname":"f2fe73ab-c6e2-40f5-b311-9227b0493443","codeMode":"markdown"}-->
```md
* `_`: Lodash v4.17.21
```

<!--{"pinCode":false,"dname":"08696e36-4a30-470e-8094-feb2f94cd126","codeMode":"markdown"}-->
```md
### React & UI components
```

<!--{"pinCode":false,"dname":"3f81e16d-08aa-4543-9270-8342029789b4","codeMode":"markdown"}-->
```md
* `Antd`: Ant Design v4.16.13
* `AntdIcons`: @ant-design/icons ^5.0.1
* `React`: React ^17.0.1
* `react`: React wrapper function used for rendering React components.
```

<!--{"pinCode":false,"dname":"81dc2c3b-3d5c-4451-875b-8789c7efdbde","codeMode":"markdown"}-->
```md
## Examples
```

<!--{"pinCode":false,"dname":"b9ac38bf-43ea-4e1d-833a-555683e6273a","codeMode":"markdown"}-->
```md
### Hello, world!
```

````
<!--{"pinCode":false,"dname":"07120854-6c51-47b9-a083-0767ebdae916","codeMode":"js","hide":false}-->
```js
{
  return await Button("Hello, world!", async () => {
    console.log("Hello, world!");
  });
}
```
````

<!--{"pinCode":false,"dname":"70db8066-08e5-4616-834a-72153d931a25","codeMode":"markdown"}-->
```md
### Multiple cells + interleaved Markdown
```

````
# Hello, world!

<!--{"pinCode":false,"dname":"07120854-6c51-47b9-a083-0767ebdae918","codeMode":"js","hide":false}-->
```js
{
  return await Button("Hello, world!", async () => {
    console.log("Hello, world!");
  });
}
```

## Here's another cell which computes a primitive value.

<!--{"pinCode":false,"dname":"reacting-to-graph-data-change-events","codeMode":"js","hide":false}-->
```js
{
  return 1 + 1;
}
```

This is the bottom of the file.
````

<!--{"pinCode":false,"dname":"6d77fa29-f9ad-4a73-95ac-3ad403666645","codeMode":"markdown"}-->
```md
### A cell which returns a combination of components
```

````
<!--{"pinCode":false,"dname":"07120854-6c51-47b9-a083-0767ebdae919","codeMode":"js","hide":false}-->
```js
{
  return html`${await Button("Hello, world!", async () => {
    console.log("Hello, world!");
  })} ${await Button("Hello, world!", async () => {
    console.log("Hello, world!");
  })} ${Inputs.button("Hi")}`;
}
```
````

<!--{"pinCode":false,"dname":"c53d45cd-3ac2-4ffc-9dc7-1e05fd13625b","codeMode":"markdown"}-->
```md
## State Management
```

<!--{"pinCode":false,"dname":"62294908-3bc5-487a-9f30-9dc7123bdd10","codeMode":"markdown"}-->
```md
In **Grove**, the **Directed Acyclic Graph (DAG)** is the architectural foundation of its reactive runtime. Unlike traditional linear notebooks, where code execution depends on the order of cells on the page, Grove treats each cell as a node in a dataflow graph.
```

<!--{"pinCode":false,"dname":"1f821149-4d28-4d70-8658-b11ce0eb98f1","codeMode":"markdown"}-->
```md
### Key Characteristics of the Grove DAG
```

<!--{"pinCode":false,"dname":"0bc66b98-d0bf-4dde-92e3-b378ed279891","codeMode":"markdown"}-->
```md
* **Dependency-Based Execution:** Cells are executed based on their topological order. If Cell B references a variable defined in Cell A, a directed edge is created from A to B ((A \to B)). Cell B will only run after Cell A has successfully evaluated.
* **Reactivity:** When a value in a "parent" cell changes (e.g., via an input slider), the Grove runtime automatically propagates that change through the DAG, re-evaluating only the "downstream" cells.
* **Acyclic Constraint:** The graph must be "acyclic." Circular dependencies (e.g., Cell A depends on B, which depends on A) are prohibited and will cause the Grove runtime to throw an error.
* **Order Independence:** Because the DAG determines execution, the physical position of cells in Grove does not matter. A variable defined at the bottom of the page can be used at the top; the runtime handles the sequence correctly.
```

<!--{"pinCode":false,"dname":"30521184-0f81-430c-b7dd-f3361eec2966","codeMode":"markdown"}-->
```md
### Implicit Handling of Promises and Generators
```

<!--{"pinCode":false,"dname":"d40a7ad9-bedb-4a31-9e86-b02cf3e57e8e","codeMode":"markdown"}-->
```md
The Grove DAG also manages asynchronous state. If a cell returns a **Promise**, downstream cells in the DAG implicitly wait for it to resolve. If a cell is a **Generator**, the DAG triggers a re-evaluation of all dependent cells every time a new value is yielded.
```

<!--{"pinCode":false,"dname":"31ad85c4-b224-4605-a33f-0ad576a1f3e0","codeMode":"markdown"}-->
```md
### State Management Examples
```

<!--{"pinCode":false,"dname":"e5f584e7-0ce1-446d-8a3c-7cf4c508f39f","codeMode":"markdown"}-->
```md
#### Basic reactive variable
```

````
<!--{"pinCode":false,"dname":"reactive-variable-cell1","codeMode":"js","hide":false}-->
```js
x = {
  return 1 + 1;
}
```

<!--{"pinCode":false,"dname":"reactive-variable-cell2","codeMode":"js","hide":false}-->
```js
y = {
  return x + 2;
}
```
````

<!--{"pinCode":false,"dname":"01a657bc-3067-46ee-9c65-035637d443f3","codeMode":"markdown"}-->
```md
#### Reactive variable with a promise
```

````
<!--{"pinCode":false,"dname":"reactive-variable-cell3","codeMode":"js","hide":false}-->
```js
z = {
  return await fetch("https://api.example.com/data");
}
```

<!--{"pinCode":false,"dname":"reactive-variable-cell4","codeMode":"js","hide":false}-->
```js
w = {
  return (await z).json();
}
```
````

<!--{"pinCode":false,"dname":"8b5d0328-f039-4e75-ae00-4d440c969f9a","codeMode":"markdown"}-->
```md
#### viewof
```

<!--{"pinCode":false,"dname":"fb4c09f7-afa9-4d76-a62f-572a99d5ef00","codeMode":"markdown"}-->
```md
A cell which declares a viewof variable is a reactive variable.
```

````
<!--{"pinCode":false,"dname":"reactive-variable-cell5","codeMode":"js","hide":false}-->
```js
viewof x = Inputs.text({label: "Name", placeholder: "What's your name?"});
```
````

<!--{"pinCode":false,"dname":"55905e9a-b7b6-4129-a20d-7bf486114084","codeMode":"markdown"}-->
```md
### mutable variable
```

<!--{"pinCode":false,"dname":"544a326b-642c-4f70-ac50-dc9249a194e4","codeMode":"markdown"}-->
```md
A ⁠mutable cell allows you to break the standard functional flow of the DAG by creating a variable that can be updated via assignment from other cells. While normal cells are "read-only" to their neighbors, a mutable variable provides a controlled way to handle state that changes in response to events or specific logic.
```

````
<!--{"pinCode":false,"dname":"mutable-variable-cell1","codeMode":"js","hide":false}-->
```js
mutable counter = 0
```

<!--{"pinCode":false,"dname":"mutable-variable-cell2","codeMode":"js","hide":false}-->
```js
Button("Increment", async () => {
    mutable counter = counter + 1;
});
```
````

<!--{"pinCode":false,"dname":"5c7ee517-cba9-49a6-9f31-7a120a2071f2","codeMode":"markdown"}-->
```md
## Best Practices
```

<!--{"pinCode":false,"dname":"9d11f2ab-c4bd-4946-9bd3-8034bf4129f0","codeMode":"markdown"}-->
```md
* Prefer AntD components.
```
