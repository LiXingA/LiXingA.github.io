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

<!--{"pinCode":true,"dname":"2c65cc2a-173f-4170-8fdf-944c81b9c2ed","codeMode":"js"}-->
```js
import { db } from './9.md'
```

<!--{"pinCode":true,"dname":"dda08478-e3ca-4480-8ece-7ae94ac67658","codeMode":"js"}-->
```js
db
```

<!--{"pinCode":true,"dname":"623cb48f-3f88-48dc-88b3-ccda6264f258","codeMode":"js"}-->
```js
viewof select = render(({ useSetter }) => {
    const { Select } = Antd;
    const handleChange = (value) => {
        console.log(`selected ${value}`);
    };
    useSetter({});
    return jsx`<${Select} key='cc9984ab-ca4c-4f07-88d6-2ebd939d8d54'
        defaultValue="lucy"
        style=${{ width: 120 }}
        onChange=${handleChange}
        options=${[
            { value: "jack", label: "Jack" },
            { value: "lucy", label: "Lucy" },
            { value: "disabled", disabled: true, label: "Disabled" },
            { value: "Yiminghe", label: "yiminghe" },
        ]}
    />`;
})
```
