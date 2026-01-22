``` plotChart
{
 "dataTypes": {
  "species": {
   "type": "string"
  },
  "island": {
   "type": "string"
  },
  "culmen_length_mm": {
   "type": "number"
  },
  "culmen_depth_mm": {
   "type": "number"
  },
  "flipper_length_mm": {
   "type": "number"
  },
  "body_mass_g": {
   "type": "number"
  },
  "sex": {
   "type": "string"
  }
 },
 "dname": "5476925c-01e3-4bca-8c1a-d04a08747278",
 "customise": {
  "title": "",
  "subtitle": "",
  "caption": "",
  "height": "",
  "widthType": "auto",
  "width": 300,
  "marginTop": "",
  "marginRight": "",
  "marginBottom": "",
  "marginLeft": "",
  "insetTop": "",
  "insetRight": "",
  "insetBottom": "",
  "insetLeft": "",
  "xLabel": "",
  "xScale": "",
  "xOptions": [],
  "yLabel": "",
  "yScale": "",
  "yOptions": [],
  "colorLegend": true,
  "colorScheme": "",
  "colorScale": "",
  "colorOptions": []
 },
 "marks": {
  "xf": "",
  "x": "sex",
  "yf": "",
  "y": "body_mass_g",
  "colorf": "",
  "color": "",
  "sizef": "",
  "size": "",
  "fx": "",
  "fy": "",
  "mark": "dot"
 },
 "selectedCategoryFrom": "files",
 "selectedCategory": "tutorial/files/penguins.csv"
}
```

<!--{"pinCode":true,"dname":"b581638c-6e1f-40a2-82ef-7cad061be228","codeMode":"js"}-->
```js
123456
```

<!--{"pinCode":false,"dname":"3e64983a-86c1-46aa-83dd-d0a88b0f227a","codeMode":"htmlmixed"}-->
```html
<div style="color: grey; font: 13px/25.5px var(--sans-serif); text-transform: uppercase;"><h1 style="display: none;">Plot: Histogram</h1><a href="/graphxr/graphxr/graphxr/plot">Observable Plot</a> › <a href="/graphxr/graphxr/graphxr/@observablehq/plot-gallery">Gallery</a></div>
```

<!--{"type":"header","level":1}-->
# Histogram

<!--{"type":"paragraph"}-->
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
