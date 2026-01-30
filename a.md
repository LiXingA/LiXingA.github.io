# <<<<<<< HEAD 2323

<!--{"pinCode":true,"dname":"c1918cd7-3e3a-42ba-a11f-69ca3f97c278","codeMode":"js"}-->
```js
123
```

<!--{"pinCode":false,"dname":"121b641a-d327-4707-878b-6686f2729d10","codeMode":"markdown"}-->
> > > > > > > d3bb76fed00c0798ced868f35ffa53a66b9852fe

# SQL + Chart

Using ${Link("sqlite/sqlite", "SQLite")} and undefined. Other ${Link("databases/databases", "database clients")} are available.

<!--{"pinCode":false,"dname":"c66daf02-531b-436f-9ca0-5359d3a5ff0b","codeMode":"js"}-->
```js
database = (FileAttachment("chinook.db").sqlite())
```

<!--{"pinCode":false,"dname":"1d2b8867-9448-4c93-bbdd-c52286b39d2d","codeMode":"js"}-->
```js
query = (__query.sql(database,invalidation,"database")`SELECT * FROM tracks`)
```

<!--{"pinCode":false,"dname":"87d433b7-82f2-4ac7-8ab3-d5bd374741eb","codeMode":"js"}-->
```js
Plot.plot({
  caption: "What are the common lengths of songs?",
  x: {
    transform: d => d / 1000 / 60,
    label: "Minutes (s) →"
  },
  marks: [
    Plot.ruleY([0]),
    Plot.rectY(query, Plot.binX({y: "sum"}, {x: "Milliseconds"}))
  ]
})
```
