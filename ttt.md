<!--{"pinCode":true,"dname":"8c136282-b238-4228-8252-b99b7d3d0ea8","codeMode":"js"}-->
```js
12345
```

<!--{"pinCode":false,"dname":"3e64983a-86c1-46aa-83dd-d0a88b0f227a","codeMode":"markdown"}-->
<div style="color: grey; font: 13px/25.5px var(--sans-serif); text-transform: uppercase;"><h1 style="display: none;">Plot: Histogram</h1><a href="/graphxr/plot">Observable Plot</a> › <a href="/graphxr/@observablehq/plot-gallery">Gallery</a></div>

# Histogram

Using the [bin transform](/plot/transforms/bin) and [rect mark](/plot/marks/rect).

<!--{"pinCode":false,"dname":"c1e6f863-c7f7-4571-aceb-765b192cc9d0","codeMode":"js"}-->
```js
data = (FileAttachment("penguins.csv").csv({typed: true}))
```

<!--{"pinCode":false,"dname":"eee26a64-81ce-493e-aac7-f3ee54e6f9ad","codeMode":"js"}-->
```js
Plot.plot({
  y: {grid: true},
  color: {legend: true},
  marks: [
    Plot.rectY(data, Plot.binX({y: "count"}, {x: "flipper_length_mm", fill: "sex"})),
    Plot.ruleY([0])
  ]
})
```
