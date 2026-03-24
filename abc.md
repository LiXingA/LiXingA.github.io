<!--{"pinCode":true,"dname":"d4b1cebf-7940-4ebf-8ade-485bd2600ac9","codeMode":"javascript"}-->
```javascript
var a = 123
```

<!--{"pinCode":true,"dname":"e9198995-9487-40ec-88a9-3e3dce429347","codeMode":"jsx"}-->
```jsx
12456
```

<!--{"pinCode":true,"dname":"8b7e2244-ae8d-4c6e-a86e-c53e0277c86b","codeMode":"js"}-->
```js
a = 123
```

``` antChart
{
 "chartConfigs": {
  "895c11a9-7fd1-4b6b-9d3c-1c680d64e155": {
   "chartKey": "895c11a9-7fd1-4b6b-9d3c-1c680d64e155",
   "createTime": 1769764882568,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "reD": {
    "dbTable": true,
    "query": "",
    "selectedTable": "names",
    "filters": [
     {}
    ],
    "selectedColumns": [
     "state",
     "gender",
     "year",
     "name",
     "number"
    ],
    "sorts": [
     {}
    ],
    "slice": {
     "to": 1000,
     "from": 0
    }
   },
   "neo": {
    "selectionType": "",
    "nodeLabel": "",
    "propertyName": "",
    "propertyValue": ""
   },
   "plotCode": "",
   "text": "",
   "selectedCategoryFrom": "files",
   "selectedCategory": "files/names.db",
   "selectedProperties": [
    "year",
    "number"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "createColumns": {},
   "configColumns": {},
   "hideColumns": [],
   "chartColumns": [],
   "type": "Basic Scatter",
   "options": {
    "yField": "number",
    "smooth": false,
    "xAxis": {
     "title": {
      "text": "year",
      "autoRotate": true
     },
     "label": {
      "offset": 10,
      "offsetX": 0,
      "offsetY": 0,
      "rotate": {
       "displayConfig": {
        "type": "Number"
       },
       "minV": 0,
       "maxV": 10,
       "step": 0.01,
       "value": 0
      },
      "autoRotate": false,
      "autoHide": true,
      "style": {
       "displayConfig": {
        "type": "Off"
       },
       "fontSize": 10,
       "textAlign": {
        "displayConfig": {
         "type": "Select"
        },
        "selector": [
         "left",
         "center",
         "right"
        ],
        "value": "center"
       },
       "fill": {
        "displayConfig": {
         "type": "Off",
         "onValue": {
          "displayConfig": {
           "type": "Color"
          },
          "value": "var(--text-color)"
         }
        }
       }
      }
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "Off"
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     },
     "min": {
      "displayConfig": {
       "type": "Off",
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "Off",
       "onValue": 5
      }
     }
    },
    "yAxis": {
     "title": {
      "text": "number",
      "autoRotate": true
     },
     "label": {
      "offset": 10,
      "offsetX": 0,
      "offsetY": 0,
      "rotate": {
       "displayConfig": {
        "type": "Number"
       },
       "minV": 0,
       "maxV": 10,
       "step": 0.01,
       "value": 0
      },
      "autoRotate": false,
      "autoHide": true,
      "style": {
       "displayConfig": {
        "type": "Off"
       },
       "fontSize": 10,
       "textAlign": {
        "displayConfig": {
         "type": "Select"
        },
        "selector": [
         "left",
         "center",
         "right"
        ],
        "value": "center"
       },
       "fill": {
        "displayConfig": {
         "type": "Off",
         "onValue": {
          "displayConfig": {
           "type": "Color"
          },
          "value": "var(--text-color)"
         }
        }
       }
      }
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On"
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     },
     "min": {
      "displayConfig": {
       "type": "On",
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "Off",
       "onValue": 5
      }
     }
    }
   }
  },
  "b0b8b864-31c5-44cc-bd55-a5bb0b8df278": {
   "chartKey": "b0b8b864-31c5-44cc-bd55-a5bb0b8df278",
   "createTime": 1769765162118,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "reD": {
    "dbTable": true,
    "query": "",
    "selectedTable": "names",
    "filters": [
     {}
    ],
    "selectedColumns": [
     "state",
     "gender",
     "year",
     "name",
     "number"
    ],
    "sorts": [
     {}
    ],
    "slice": {
     "to": 1000,
     "from": 0
    }
   },
   "mongo": {
    "collectionName": "",
    "filter": {},
    "filterTmp": {},
    "filterStr": "{}",
    "projection": {},
    "projectionStr": "{}",
    "column": [],
    "lowerBound": "min",
    "upperBound": "max",
    "isObjectId": true,
    "limit": 1000,
    "sort": {},
    "sortStr": "{}",
    "skip": 0
   },
   "dynamo": {
    "tab": 0,
    "scanFilterTmp": [
     {}
    ],
    "scanFilterStr": "{}",
    "TableName": "",
    "IndexName": "",
    "Select": "ALL_ATTRIBUTES",
    "AttributesToGet": [],
    "ConditionalOperator": "AND",
    "ScanFilter": {},
    "Limit": 1000
   },
   "neo": {
    "selectionType": "",
    "nodeLabel": "",
    "propertyName": "",
    "propertyValue": ""
   },
   "plotCode": "",
   "text": "",
   "selectedCategoryFrom": "files",
   "selectedCategory": "files/names.db",
   "selectedProperties": [
    "year",
    "number"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "createColumns": {},
   "configColumns": {},
   "hideColumns": [],
   "chartColumns": [],
   "type": "Stack Histogram",
   "options": {
    "binField": "number",
    "stackField": "year"
   }
  },
  "a709dc29-e6af-4d17-a818-344817030226": {
   "chartKey": "a709dc29-e6af-4d17-a818-344817030226",
   "createTime": 1769765347534,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "reD": {
    "dbTable": true,
    "query": "",
    "selectedTable": "names",
    "filters": [
     {}
    ],
    "selectedColumns": [
     "state",
     "gender",
     "year",
     "name",
     "number"
    ],
    "sorts": [
     {}
    ],
    "slice": {
     "to": 1000,
     "from": 0
    }
   },
   "neo": {
    "selectionType": "",
    "nodeLabel": "",
    "propertyName": "",
    "propertyValue": ""
   },
   "plotCode": "",
   "text": "",
   "selectedCategoryFrom": "files",
   "selectedCategory": "files/names.db",
   "selectedProperties": [
    "number",
    "year"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "createColumns": {},
   "configColumns": {},
   "hideColumns": [],
   "chartColumns": [],
   "type": "Basic Scatter",
   "options": {
    "xField": "number",
    "yField": "year",
    "smooth": false,
    "xAxis": {
     "title": {
      "text": "number",
      "autoRotate": true
     },
     "label": {
      "offset": 10,
      "offsetX": 0,
      "offsetY": 0,
      "rotate": {
       "displayConfig": {
        "type": "Number"
       },
       "minV": 0,
       "maxV": 10,
       "step": 0.01,
       "value": 0
      },
      "autoRotate": false,
      "autoHide": true,
      "style": {
       "displayConfig": {
        "type": "Off"
       },
       "fontSize": 10,
       "textAlign": {
        "displayConfig": {
         "type": "Select"
        },
        "selector": [
         "left",
         "center",
         "right"
        ],
        "value": "center"
       },
       "fill": {
        "displayConfig": {
         "type": "Off",
         "onValue": {
          "displayConfig": {
           "type": "Color"
          },
          "value": "var(--text-color)"
         }
        }
       }
      }
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "Off"
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     },
     "min": {
      "displayConfig": {
       "type": "Off",
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "Off",
       "onValue": 5
      }
     }
    },
    "yAxis": {
     "title": {
      "text": "year",
      "autoRotate": true
     },
     "label": {
      "offset": 10,
      "offsetX": 0,
      "offsetY": 0,
      "rotate": {
       "displayConfig": {
        "type": "Number"
       },
       "minV": 0,
       "maxV": 10,
       "step": 0.01,
       "value": 0
      },
      "autoRotate": false,
      "autoHide": true,
      "style": {
       "displayConfig": {
        "type": "Off"
       },
       "fontSize": 10,
       "textAlign": {
        "displayConfig": {
         "type": "Select"
        },
        "selector": [
         "left",
         "center",
         "right"
        ],
        "value": "center"
       },
       "fill": {
        "displayConfig": {
         "type": "Off",
         "onValue": {
          "displayConfig": {
           "type": "Color"
          },
          "value": "var(--text-color)"
         }
        }
       }
      }
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On"
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     },
     "min": {
      "displayConfig": {
       "type": "On",
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "Off",
       "onValue": 5
      }
     }
    }
   }
  },
  "87c532f3-a60d-4aa4-b1bf-7565c80b810b": {
   "chartKey": "87c532f3-a60d-4aa4-b1bf-7565c80b810b",
   "createTime": 1769765397361,
   "renderType": "Chart",
   "active": true,
   "globalFilterKey": "files#files/names.db#names",
   "fetchPeriod": 0,
   "reD": {
    "dbTable": true,
    "query": "",
    "selectedTable": "names",
    "filters": [
     {}
    ],
    "selectedColumns": [
     "state",
     "gender",
     "year",
     "name",
     "number"
    ],
    "sorts": [
     {}
    ],
    "slice": {
     "to": 1000,
     "from": 0
    }
   },
   "neo": {
    "selectionType": "",
    "nodeLabel": "",
    "propertyName": "",
    "propertyValue": ""
   },
   "plotCode": "",
   "text": "",
   "selectedCategoryFrom": "files",
   "selectedCategory": "files/names.db",
   "selectedProperties": [
    "year",
    "number"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "createColumns": {},
   "configColumns": {},
   "hideColumns": [],
   "chartColumns": [],
   "type": "Stack Histogram",
   "options": {
    "binField": "number",
    "stackField": "year"
   }
  }
 },
 "layouts": {
  "lg": [
   {
    "w": 6,
    "h": 12,
    "x": 0,
    "y": 0,
    "i": "895c11a9-7fd1-4b6b-9d3c-1c680d64e155",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 12,
    "x": 6,
    "y": 0,
    "i": "b0b8b864-31c5-44cc-bd55-a5bb0b8df278",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 12,
    "x": 0,
    "y": 12,
    "i": "a709dc29-e6af-4d17-a818-344817030226",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 12,
    "x": 6,
    "y": 12,
    "i": "87c532f3-a60d-4aa4-b1bf-7565c80b810b",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 4,
    "x": 0,
    "y": 24,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ],
  "sm": [],
  "xxs": []
 },
 "dname": "f56f4202-d4eb-4a67-ba92-6026d5cc4d2d",
 "lock": false,
 "breakPoints": {
  "lg": 1200,
  "sm": 768,
  "xxs": 0
 }
}
```

<!--{"pinCode":false,"dname":"bd2b9d7d-1064-42bd-8e88-c5f3c2b6b939","codeMode":"markdown"}-->
##### abc

<!--{"pinCode":false,"dname":"70da9823-259b-42c3-ac9f-8d02cebb4fba","codeMode":"markdown"}-->
# Search + Table

<!--{"pinCode":false,"dname":"2f437ade-4b5c-447d-b507-e07cd395b00b","codeMode":"markdown"}-->
Using undefined and undefined. Data from <a href="https://catalog.data.gov/dataset/most-popular-baby-names" target="_blank" title="California Department of Public Health">CDPH</a>.

<!--{"pinCode":false,"dname":"934f751c-48dd-4c42-9b3c-dafcb93ef57a","codeMode":"js"}-->
```js
data = (FileAttachment("baby_names.csv").csv({typed: true}))
```

<!--{"pinCode":false,"dname":"492283f0-a46a-4aaa-8668-ae0451eecdfa","codeMode":"js"}-->
```js
viewof search = (Inputs.search(data))
```

<!--{"pinCode":false,"dname":"7e03854b-fb6a-46d6-8bcc-944ef2a8f8d3","codeMode":"js"}-->
```js
Inputs.table(search, {
  format: {
    Year: d3.format("d") // format as "1960" rather than "1,960"
  }
=======
<!--{"pinCode":true,"dname":"e0ad77db-c830-4645-a673-5351ce81e816","codeMode":"markdown"}-->
123456

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
