<!--{"pinCode":false,"dname":"1a36c614-a330-451d-acc5-3ae84d224d40","codeMode":"markdown"}-->
```md
# Plot World Map
```

<!--{"pinCode":false,"dname":"212c1063-c325-407d-98dc-07e9a2d4818b","codeMode":"js"}-->
```js
Plot.plot({
  projection: "equal-earth",
  width,
  marks: [
    Plot.geo(land, { fill: "#000" }),
    Plot.graticule(),
    Plot.sphere()
  ]
})
```

<!--{"pinCode":false,"dname":"864d4a4e-1b4e-44ca-8a68-dcf0bd77118f","codeMode":"js"}-->
```js
land = (topojson.feature(land50m, land50m.objects.land))
```

<!--{"pinCode":false,"dname":"19ffe434-9d3b-46b8-b249-c95b937365d5","codeMode":"js"}-->
```js
land50m = (FileAttachment("land-50m.json").json())
```
