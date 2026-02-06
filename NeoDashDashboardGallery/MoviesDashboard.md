<!--{"blockType":"header"}-->
## Overview

``` antChart
{
 "chartConfigs": {
  "b7be93fb-3837-4c65-8f99-1bb1746537f3": {
   "chartKey": "b7be93fb-3837-4c65-8f99-1bb1746537f3",
   "createTime": 1698235723986,
   "renderType": "Markdown",
   "active": true,
   "fetchPeriod": 0,
   "text": "The *Movies Database* is a great way to get to know Neo4j and Cypher. This graph contains the following data:\n- `Person` nodes with two properties (`name` and `born`).\n- `Movie` nodes with four properties (`title`, `tagline`, `released` and `votes`).\n- Five relationship types between `Person` and `Movie` (`ACTED_IN`,  `DIRECTED`, `PRODUCED`, `WROTE`, `FOLLOWS`)\n- One relationship type between different person nodes - `FOLLOWS`.\n\nThis dashboard uses the sample dataset from the Neo4j developer guide.\n[https://neo4j.com/developer/example-data/](https://neo4j.com/developer/example-data/)\n\n____\n\n\nYou will find two pages in this same dashboard:\n1. An **Overview** page with general info about the graph.\n3. An **Actor view** page that lets you drill down on a specific person.\n\nTo inspect the Cypher behind each of the visualizations, click the (⋮) button on the top right of a report. This lets you see and edit the query.",
   "selectedCategoryFrom": "",
   "selectedCategory": "",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "The Movies Dashboard",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   }
  },
  "287b6b87-6aee-495b-93a6-18e826ef002e": {
   "chartKey": "287b6b87-6aee-495b-93a6-18e826ef002e",
   "createTime": 1698235880066,
   "renderType": "SingleValue",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (n)\nRETURN COUNT(n) as Total",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Total movies",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   },
   "selectedClientType": "Neo4j"
  },
  "1f00c0d9-098b-430c-b7f8-22725eb2bf57": {
   "chartKey": "1f00c0d9-098b-430c-b7f8-22725eb2bf57",
   "createTime": 1698238236871,
   "renderType": "SingleValue",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (n:Person)\nRETURN COUNT(n)",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Total people",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   },
   "selectedClientType": "Neo4j"
  },
  "94e40aa4-4a69-4668-a7e1-beb8a0c7cd6b": {
   "chartKey": "94e40aa4-4a69-4668-a7e1-beb8a0c7cd6b",
   "createTime": 1698238320497,
   "renderType": "SingleValue",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH ()-[r]->()\nRETURN count(r)",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Relationships",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   },
   "selectedClientType": "Neo4j"
  },
  "598cccc7-7933-4d54-b8d3-854bd8017791": {
   "chartKey": "598cccc7-7933-4d54-b8d3-854bd8017791",
   "createTime": 1698238423882,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH ()-[r]->()\nRETURN type(r) as Relationship, COUNT(r) as Total"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [
    "Relationship",
    "Total"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "Basic Column",
   "options": {
    "xField": "Relationship",
    "yField": "Total",
    "title": {
     "text": "Relationship types",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "legend": {
     "displayConfig": {
      "type": "Remove",
      "offValue": false
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "top-left",
       "top-right",
       "left",
       "left-top",
       "left-bottom",
       "right",
       "right-top",
       "right-bottom",
       "bottom",
       "bottom-left",
       "bottom-right"
      ],
      "value": "top-left"
     },
     "flipPage": true,
     "offsetX": 0,
     "offsetY": 0
    },
    "label": {
     "displayConfig": {
      "type": "Off"
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "bottom",
       "middle",
       "left",
       "right"
      ],
      "value": "top"
     },
     "offset": 0,
     "offsetX": 0,
     "offsetY": 0
    },
    "tooltip": {
     "displayConfig": {
      "type": "Off",
      "offValue": {
       "showContent": false,
       "shared": false
      }
     },
     "showContent": true,
     "offset": 0
    },
    "xAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "Relationship",
      "autoRotate": true
     },
     "label": {
      "offset": 40,
      "offsetX": 0,
      "offsetY": -10,
      "rotate": {
       "displayConfig": {
        "type": "Number"
       },
       "minV": 0,
       "maxV": 10,
       "step": 0.01,
       "value": 0.4
      },
      "autoRotate": false,
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On",
       "offValue": null
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     }
    },
    "yAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "Total",
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
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On",
       "offValue": null
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     }
    },
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "d0632e51-ee91-4e62-a243-311dc1bd1971": {
   "chartKey": "d0632e51-ee91-4e62-a243-311dc1bd1971",
   "createTime": 1698242577775,
   "renderType": "Graph",
   "active": true,
   "fetchPeriod": 0,
   "text": "// It's the entire graph!\nMATCH (a)-[r]->(b)\nRETURN *",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "The entire graph",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   },
   "neo": {
    "query": "// It's the entire graph!\nMATCH (a)-[r]->(b)\nRETURN *",
    "selection": {
     "Person": "(id)",
     "Movie": "released"
    },
    "labelProperty": "roles"
   },
   "selectedClientType": "Neo4j"
  },
  "939916aa-0ebe-4142-98c9-aa180177fcd2": {
   "chartKey": "939916aa-0ebe-4142-98c9-aa180177fcd2",
   "createTime": 1698243072760,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (m:Movie)<-[:ACTED_IN]-(p:Person)\nRETURN m.title as Movie, COUNT(p) as Actors\nORDER BY Actors\nDESC LIMIT 10"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [
    "Movie",
    "Actors"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "Basic Pie",
   "options": {
    "angleField": "Actors",
    "colorField": "Movie",
    "title": {
     "text": "Movies with most actors",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "label": {
     "type": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "inner",
       "outer",
       "spider"
      ],
      "value": "spider"
     },
     "content": {
      "displayConfig": {
       "type": "On",
       "onValue": "{name}\t{percentage}"
      }
     },
     "style": {
      "fontSize": 14,
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
      }
     }
    },
    "legend": {
     "displayConfig": {
      "type": "Off",
      "offValue": false
     },
     "layout": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "horizontal",
       "vertical"
      ],
      "props": {
       "allowClear": true
      }
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "top-left",
       "top-right",
       "left",
       "left-top",
       "left-bottom",
       "right",
       "right-top",
       "right-bottom",
       "bottom",
       "bottom-left",
       "bottom-right"
      ],
      "value": "right",
      "props": {
       "allowClear": true
      }
     }
    },
    "color": {
     "displayConfig": {
      "type": "Off",
      "onValue": [
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#5B8FF9"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#5AD8A6"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#5D7092"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#F6BD16"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#E8684A"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#F43D17"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#30D3A6"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#687B22"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#A24141"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#B28A37"
       }
      ]
     }
    },
    "interactions": [
     {
      "type": "element-active"
     }
    ],
    "appendPadding": 40,
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "bb148f6c-81d4-4624-b4d5-299efd1af1c3": {
   "chartKey": "bb148f6c-81d4-4624-b4d5-299efd1af1c3",
   "createTime": 1698244894521,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (m:Movie)\nRETURN toInteger(m.released/10)*10 as Year, COUNT(m) as Total\nORDER BY Year ASC\n\n\n"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [
    "Year",
    "Total"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "Basic Line",
   "options": {
    "xField": "Year",
    "yField": "Total",
    "title": {
     "text": "Movies by decade",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "smooth": true,
    "legend": {
     "displayConfig": {
      "type": "Remove",
      "offValue": false
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "top-left",
       "top-right",
       "left",
       "left-top",
       "left-bottom",
       "right",
       "right-top",
       "right-bottom",
       "bottom",
       "bottom-left",
       "bottom-right"
      ],
      "value": "top-left"
     },
     "flipPage": true,
     "offsetX": 0,
     "offsetY": 0
    },
    "lineStyle": {
     "displayConfig": {
      "type": "On"
     },
     "lineWidth": 2
    },
    "label": {
     "displayConfig": {
      "type": "Off"
     },
     "offset": 10,
     "offsetX": 0,
     "offsetY": 0
    },
    "point": {
     "displayConfig": {
      "type": "On"
     },
     "size": 5,
     "shape": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "circle",
       "point",
       "square",
       "diamond",
       "hexagon",
       "triangle",
       "cross"
      ],
      "value": "point"
     }
    },
    "tooltip": {
     "displayConfig": {
      "type": "Off",
      "offValue": {
       "showContent": false,
       "shared": false
      }
     },
     "showContent": true,
     "offset": 0
    },
    "xAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "Year",
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
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On",
       "offValue": null
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
       "offValue": false,
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "Off",
       "offValue": false,
       "onValue": 1
      }
     }
    },
    "yAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "Total",
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
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On",
       "offValue": null
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
       "offValue": false,
       "onValue": 0
      }
     },
     "tickInterval": {
      "displayConfig": {
       "type": "On",
       "offValue": false,
       "onValue": 2
      }
     }
    },
    "color": {
     "displayConfig": {
      "type": "On",
      "onValue": {
       "displayConfig": {
        "type": "Color"
       },
       "value": "#7ed321"
      }
     }
    },
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "2d9b253a-19e5-49d9-ae07-b22162ad7d43": {
   "chartKey": "2d9b253a-19e5-49d9-ae07-b22162ad7d43",
   "createTime": 1698286507150,
   "renderType": "Table",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (m:Movie)\nRETURN m.title as Movie, m.released as Year\n\n\n",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Browse the movies",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "pageSize": 5,
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "9678aae4-b829-46fd-aac9-2b4bc249c171": {
   "chartKey": "9678aae4-b829-46fd-aac9-2b4bc249c171",
   "createTime": 1698296979232,
   "renderType": "Chart",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (m:Movie)<-[r]-(p:Person)\nWHERE m.title CONTAINS \"Matrix\"\nRETURN \nm.title as Movie, \ntype(r) as Role, \nCOUNT(p) as People\n"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [
    "Movie",
    "Role",
    "People"
   ],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "Multi Column",
   "options": {
    "xField": "Role",
    "yField": "People",
    "title": {
     "text": "Customized, grouped bar chart",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "legend": {
     "displayConfig": {
      "type": "On",
      "offValue": false
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "top-left",
       "top-right",
       "left",
       "left-top",
       "left-bottom",
       "right",
       "right-top",
       "right-bottom",
       "bottom",
       "bottom-left",
       "bottom-right"
      ],
      "value": "top-left"
     },
     "flipPage": true,
     "offsetX": 0,
     "offsetY": 0
    },
    "label": {
     "displayConfig": {
      "type": "On"
     },
     "position": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "top",
       "bottom",
       "middle",
       "left",
       "right"
      ],
      "value": "top"
     },
     "offset": 0,
     "offsetX": 0,
     "offsetY": 0
    },
    "tooltip": {
     "displayConfig": {
      "type": "Off",
      "offValue": {
       "showContent": false,
       "shared": false
      }
     },
     "showContent": true,
     "offset": 0
    },
    "xAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "Role",
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
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "Off",
       "offValue": null
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     }
    },
    "yAxis": {
     "title": {
      "displayConfig": {
       "type": "Off"
      },
      "text": "People",
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
      "autoHide": true
     },
     "tickLine": {
      "displayConfig": {
       "type": "Off"
      },
      "length": 5
     },
     "grid": {
      "displayConfig": {
       "type": "On",
       "offValue": null
      },
      "line": {
       "style": {
        "lineWidth": 1
       }
      }
     }
    },
    "color": {
     "displayConfig": {
      "type": "On",
      "onValue": [
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#f8e71c"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#7ed321"
       },
       {
        "displayConfig": {
         "type": "Color"
        },
        "value": "#50e3c2"
       }
      ]
     }
    },
    "isStack": true,
    "isGroup": false,
    "isRange": false,
    "isPercent": false,
    "seriesField": "Movie",
    "data": []
   },
   "selectedClientType": "Neo4j"
  }
 },
 "layouts": {
  "lg": [
   {
    "w": 6,
    "h": 13,
    "x": 0,
    "y": 0,
    "i": "b7be93fb-3837-4c65-8f99-1bb1746537f3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 6,
    "y": 0,
    "i": "287b6b87-6aee-495b-93a6-18e826ef002e",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 8,
    "y": 0,
    "i": "1f00c0d9-098b-430c-b7f8-22725eb2bf57",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 10,
    "y": 0,
    "i": "94e40aa4-4a69-4668-a7e1-beb8a0c7cd6b",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 11,
    "x": 0,
    "y": 13,
    "i": "598cccc7-7933-4d54-b8d3-854bd8017791",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 20,
    "x": 6,
    "y": 4,
    "i": "d0632e51-ee91-4e62-a243-311dc1bd1971",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 14,
    "x": 0,
    "y": 24,
    "i": "939916aa-0ebe-4142-98c9-aa180177fcd2",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 11,
    "x": 3,
    "y": 13,
    "i": "bb148f6c-81d4-4624-b4d5-299efd1af1c3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 14,
    "x": 6,
    "y": 24,
    "i": "2d9b253a-19e5-49d9-ae07-b22162ad7d43",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 14,
    "x": 9,
    "y": 24,
    "i": "9678aae4-b829-46fd-aac9-2b4bc249c171",
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
    "y": 38,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ],
  "sm": [
   {
    "w": 3,
    "h": 4,
    "x": 0,
    "y": 12,
    "i": "b7be93fb-3837-4c65-8f99-1bb1746537f3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 0,
    "i": "287b6b87-6aee-495b-93a6-18e826ef002e",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 4,
    "i": "1f00c0d9-098b-430c-b7f8-22725eb2bf57",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 8,
    "i": "94e40aa4-4a69-4668-a7e1-beb8a0c7cd6b",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 16,
    "i": "598cccc7-7933-4d54-b8d3-854bd8017791",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 20,
    "i": "d0632e51-ee91-4e62-a243-311dc1bd1971",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 24,
    "i": "939916aa-0ebe-4142-98c9-aa180177fcd2",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 28,
    "i": "bb148f6c-81d4-4624-b4d5-299efd1af1c3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 32,
    "i": "2d9b253a-19e5-49d9-ae07-b22162ad7d43",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 36,
    "i": "9678aae4-b829-46fd-aac9-2b4bc249c171",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 40,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ],
  "xxs": [
   {
    "w": 2,
    "h": 13,
    "x": 0,
    "y": 0,
    "i": "b7be93fb-3837-4c65-8f99-1bb1746537f3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 13,
    "i": "287b6b87-6aee-495b-93a6-18e826ef002e",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 17,
    "i": "1f00c0d9-098b-430c-b7f8-22725eb2bf57",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 21,
    "i": "94e40aa4-4a69-4668-a7e1-beb8a0c7cd6b",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 9,
    "x": 0,
    "y": 25,
    "i": "598cccc7-7933-4d54-b8d3-854bd8017791",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 9,
    "x": 0,
    "y": 34,
    "i": "d0632e51-ee91-4e62-a243-311dc1bd1971",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 12,
    "x": 0,
    "y": 43,
    "i": "939916aa-0ebe-4142-98c9-aa180177fcd2",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 9,
    "x": 0,
    "y": 55,
    "i": "bb148f6c-81d4-4624-b4d5-299efd1af1c3",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 10,
    "x": 0,
    "y": 64,
    "i": "2d9b253a-19e5-49d9-ae07-b22162ad7d43",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 10,
    "x": 0,
    "y": 74,
    "i": "9678aae4-b829-46fd-aac9-2b4bc249c171",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 84,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ]
 },
 "dname": "2221947e-731a-411a-afca-3048e74d7710",
 "lock": false,
 "breakPoints": {
  "lg": 1200,
  "sm": 768,
  "xxs": 0
 }
}
```

<!--{"blockType":"header"}-->
## Actor View

``` antChart
{
 "chartConfigs": {
  "6aa374ad-869d-4c78-9c14-9805d61366f8": {
   "chartKey": "6aa374ad-869d-4c78-9c14-9805d61366f8",
   "createTime": 1698297606516,
   "renderType": "Markdown",
   "active": true,
   "fetchPeriod": 0,
   "text": "On this page, you can select a person from a table, and dynamically view other visualizations update.\n\n",
   "selectedCategoryFrom": "",
   "selectedCategory": "",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "About this page",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   }
  },
  "722b8177-5797-402b-9bd4-7fe3cb167491": {
   "chartKey": "722b8177-5797-402b-9bd4-7fe3cb167491",
   "createTime": 1698297645976,
   "renderType": "Table",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH (p:Person)--(m:Movie)\nRETURN p.name as Person, COUNT(m) as Movies \nORDER BY Movies DESC\n\n\n",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Select a person",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "pageSize": 5,
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "de1e33b7-0659-4051-a11b-a688f8b41039": {
   "chartKey": "de1e33b7-0659-4051-a11b-a688f8b41039",
   "createTime": 1698297691383,
   "renderType": "ParameterSelect",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "selectionType": "nodeProperty",
    "nodeLabel": "Person",
    "propertyName": "name",
    "propertyValue": "Tom Cruise"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Selected person",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    }
   },
   "selectedClientType": "Neo4j"
  },
  "11edbf51-29f7-4c7e-a517-7330c43a1680": {
   "chartKey": "11edbf51-29f7-4c7e-a517-7330c43a1680",
   "createTime": 1698297919108,
   "renderType": "Graph",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH path=(p:Person)--()\nWHERE p.name = $neodash_person_name\nRETURN path\n\n",
    "selection": {
     "Person": "name",
     "Movie": "title"
    },
    "labelProperty": "roles"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Graph view for this person",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "nodeColorScheme": {
     "displayConfig": {
      "type": "Select"
     },
     "selector": [
      "neodash",
      "nivo",
      "category10",
      "accent",
      "dark2",
      "paired",
      "pastel1",
      "pastel2",
      "set1",
      "set2",
      "set3"
     ],
     "value": "paired"
    },
    "nodeLabelColor": {
     "displayConfig": {
      "type": "On",
      "onValue": {
       "displayConfig": {
        "type": "Color"
       },
       "value": "#000000"
      }
     }
    },
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "aefb2638-d6a5-4a67-a456-03d7efc32965": {
   "chartKey": "aefb2638-d6a5-4a67-a456-03d7efc32965",
   "createTime": 1698298215738,
   "renderType": "Table",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH path=(p)-->(m:Movie)\nWHERE p.name = $neodash_person_name\nRETURN m.title as Movie, m.tagline as Tagline, m.released as Released\n\n",
    "selection": {},
    "labelProperty": ""
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "Movies for the selected person",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "description": {
     "text": "Enter markdown here..."
    },
    "pageSize": 5,
    "data": []
   },
   "selectedClientType": "Neo4j"
  },
  "9708ff7c-c477-4e48-a852-c32cadb9a1ae": {
   "chartKey": "9708ff7c-c477-4e48-a852-c32cadb9a1ae",
   "createTime": 1698298294390,
   "renderType": "SankeyChart",
   "active": true,
   "fetchPeriod": 0,
   "neo": {
    "query": "MATCH path=(p:Person)--(m:Movie)\nWHERE p.name = $neodash_person_name\nRETURN p, apoc.create.vRelationship(p, \"IN\", {weight: m.votes}, m), m\n\n",
    "selection": {
     "Person": "name",
     "Movie": "title"
    },
    "labelProperty": "weight"
   },
   "text": "",
   "selectedCategoryFrom": "client",
   "selectedCategory": "movies",
   "selectedProperties": [],
   "selectedDb": "",
   "chartData": [],
   "emptyFills": {},
   "castColumns": {},
   "joinColumns": {},
   "chartColumns": [],
   "type": "",
   "options": {
    "title": {
     "text": "The highest voted movies for this person",
     "size": {
      "displayConfig": {
       "type": "Select"
      },
      "selector": [
       "h1",
       "h2",
       "h3",
       "h4",
       "h5",
       "h6"
      ],
      "value": "h6"
     }
    },
    "data": []
   },
   "selectedClientType": "Neo4j"
  }
 },
 "layouts": {
  "lg": [
   {
    "w": 3,
    "h": 7,
    "x": 0,
    "y": 0,
    "i": "6aa374ad-869d-4c78-9c14-9805d61366f8",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 4,
    "h": 14,
    "x": 3,
    "y": 0,
    "i": "722b8177-5797-402b-9bd4-7fe3cb167491",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 3,
    "h": 7,
    "x": 0,
    "y": 7,
    "i": "de1e33b7-0659-4051-a11b-a688f8b41039",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 5,
    "h": 14,
    "x": 7,
    "y": 0,
    "i": "11edbf51-29f7-4c7e-a517-7330c43a1680",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 13,
    "x": 0,
    "y": 14,
    "i": "aefb2638-d6a5-4a67-a456-03d7efc32965",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 13,
    "x": 6,
    "y": 14,
    "i": "9708ff7c-c477-4e48-a852-c32cadb9a1ae",
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
    "y": 27,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ],
  "sm": [
   {
    "w": 3,
    "h": 4,
    "x": 3,
    "y": 4,
    "i": "6aa374ad-869d-4c78-9c14-9805d61366f8",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 0,
    "i": "722b8177-5797-402b-9bd4-7fe3cb167491",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 8,
    "i": "de1e33b7-0659-4051-a11b-a688f8b41039",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 12,
    "i": "11edbf51-29f7-4c7e-a517-7330c43a1680",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 16,
    "i": "aefb2638-d6a5-4a67-a456-03d7efc32965",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
    "h": 4,
    "x": 0,
    "y": 20,
    "i": "9708ff7c-c477-4e48-a852-c32cadb9a1ae",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 6,
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
  "xxs": [
   {
    "w": 2,
    "h": 7,
    "x": 0,
    "y": 0,
    "i": "6aa374ad-869d-4c78-9c14-9805d61366f8",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 12,
    "x": 0,
    "y": 7,
    "i": "722b8177-5797-402b-9bd4-7fe3cb167491",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 19,
    "i": "de1e33b7-0659-4051-a11b-a688f8b41039",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 9,
    "x": 0,
    "y": 23,
    "i": "11edbf51-29f7-4c7e-a517-7330c43a1680",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 10,
    "x": 0,
    "y": 32,
    "i": "aefb2638-d6a5-4a67-a456-03d7efc32965",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 7,
    "x": 0,
    "y": 42,
    "i": "9708ff7c-c477-4e48-a852-c32cadb9a1ae",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": true,
    "isResizable": true
   },
   {
    "w": 2,
    "h": 4,
    "x": 0,
    "y": 49,
    "i": "add",
    "minW": 2,
    "minH": 3,
    "moved": false,
    "static": false,
    "isDraggable": false,
    "isResizable": false
   }
  ]
 },
 "dname": "3bc6a983-1937-4050-9f38-4ec71f78c931",
 "lock": false,
 "breakPoints": {
  "lg": 1200,
  "sm": 768,
  "xxs": 0
 }
}
```

<!--{"pinCode":false,"dname":"59a39343-8ef0-4a68-840f-a1a865d55e70","codeMode":"js"}-->
```js
movies = createDatabaseClient({
      "name": "movies",
      "type": "Neo4j",
      "connectionHostedBy": "Client",
      "protocal": "neo4j+s",
      "host": "demo.neo4jlabs.com",
      "port": 7687,
      "user": "movies",
      "password": "movies",
      "database": "movies",
    })
```
