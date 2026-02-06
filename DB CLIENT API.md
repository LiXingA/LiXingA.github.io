## Send query example (for dynamodb client)
### AttributeValue
Grammer:
```
{ // AttributeValue Union: only one key present
  S: "STRING_VALUE",
  N: "STRING_VALUE",
  B: "BLOB_VALUE",
  SS: [ // StringSetAttributeValue
    "STRING_VALUE",
  ],
  NS: [ // NumberSetAttributeValue
    "STRING_VALUE",
  ],
  BS: [ // BinarySetAttributeValue
    "BLOB_VALUE",
  ],
  M: { // MapAttributeValue
    "<keys>": {//  Union: only one key present
      S: "STRING_VALUE",
      N: "STRING_VALUE",
      B: "BLOB_VALUE",
      SS: [
        "STRING_VALUE",
      ],
      NS: [
        "STRING_VALUE",
      ],
      BS: [
        "BLOB_VALUE",
      ],
      M: {
        "<keys>": "<AttributeValue>",
      },
      L: [ // ListAttributeValue
        "<AttributeValue>",
      ],
      NULL: true || false,
      BOOL: true || false,
    },
  },
  L: [
    "<AttributeValue>",
  ],
  NULL: true || false,
  BOOL: true || false,
}
```
### List tables
Grammer:
```
await dbClient.query(JSON.stringify({
    operationType: 0,
    params:{
      ExclusiveStartTableName: "STRING_VALUE",
      Limit: Number("int"),
    }
  }));
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
await ClientDynamo.query(JSON.stringify({ operationType: 0, params: {} }))
```
### Describe table
Grammer:
```
await dbClient.query(JSON.stringify({
      operationType: 1,
      tableName: "STRING_VALUE"
  }));
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
await ClientDynamo.query(JSON.stringify({ operationType: 1, tableName: "DL_test" }))
```
### Query
Grammer:
```
await dbClient.query(JSON.stringify({
  operationType: 2,
  params:{
    TableName: "STRING_VALUE", // required
    IndexName: "STRING_VALUE",
    Select: "ALL_ATTRIBUTES" || "ALL_PROJECTED_ATTRIBUTES" || "SPECIFIC_ATTRIBUTES" || "COUNT",
    AttributesToGet: [ // AttributeNameList
      "STRING_VALUE",
    ],
    Limit: Number("int"),
    ConsistentRead: true || false,
    KeyConditions: { // KeyConditions
      "<keys>": { // Condition
        AttributeValueList: [ // AttributeValueList
        ],
        ComparisonOperator: "EQ" || "NE" || "IN" || "LE" || "LT" || "GE" || "GT" || "BETWEEN" || "NOT_NULL" || "NULL" || "CONTAINS" || "NOT_CONTAINS" || "BEGINS_WITH", // required
      },
    },
    QueryFilter: { // FilterConditionMap
      "<keys>": {
        AttributeValueList: [
          "<AttributeValue>",
        ],
        ComparisonOperator: "EQ" || "NE" || "IN" || "LE" || "LT" || "GE" || "GT" || "BETWEEN" || "NOT_NULL" || "NULL" || "CONTAINS" || "NOT_CONTAINS" || "BEGINS_WITH", // required
      },
    },
    ConditionalOperator: "AND" || "OR",
    ScanIndexForward: true || false,
    ExclusiveStartKey: { // Key
      "<keys>": "<AttributeValue>",
    },
    ReturnConsumedCapacity: "INDEXES" || "TOTAL" || "NONE",
    ProjectionExpression: "STRING_VALUE",
    FilterExpression: "STRING_VALUE",
    KeyConditionExpression: "STRING_VALUE",
    ExpressionAttributeNames: { // ExpressionAttributeNameMap
      "<keys>": "STRING_VALUE",
    },
    ExpressionAttributeValues: { // ExpressionAttributeValueMap
      "<keys>": "<AttributeValue>",
    },
  }
}));
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
ClientDynamo.query(JSON.stringify({
  operationType: 2,
  params:{
    TableName: "DL_test",
    FilterExpression: "sample_time > :time AND device_id > :dev_id",
    ExpressionAttributeValues: {
      ":time": {N:"1685035996065"},
      ":dev_id": {N:"100004"}
    },
    ConsistentRead: true,
  }
}));
```
### Execute PartiQL
Grammer:
```
await dbClient.query(JSON.stringify({
  operationType: 3,
  params:{
    Statement: "STRING_VALUE", // required
    Parameters:[<AttributeValue>],
    ConsistentRead: true || false,
    NextToken: "STRING_VALUE",
    ReturnConsumedCapacity: "INDEXES" || "TOTAL" || "NONE",
    Limit: Number("int"),
  }
}));
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
ClientDynamo.query(JSON.stringify({
  operationType: 3,
  params:{
    Statement: `select * from DL_test where sample_time > ? AND device_id > ?`,
    Parameters: [{N:"1685481407878"},{N:"100004"}],
  }
}))
```
### Batch Execute PartiQL
Grammer:
```
await dbClient.query(JSON.stringify({
  operationType: 4,
  params:{
    Statements: [// PartiQLBatchRequest // required
      {// BatchStatementRequest
        Statement: "STRING_VALUE", // required
        Parameters:[<AttributeValue>],
        ConsistentRead: true || false,
        NextToken: "STRING_VALUE",
        ReturnConsumedCapacity: "INDEXES" || "TOTAL" || "NONE",
        Limit: Number("int"),
      }
    ]
  }
}))
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
ClientDynamo.query(JSON.stringify({
  operationType: 4,
  params:{
    Statements: [
    {
        Statement: "SELECT * FROM PepperMeasurements WHERE Unit=?",
        Parameters: [{S:"Teaspoons"}],
        ConsistentRead: true,
    },
    {
        Statement: "SELECT * FROM PepperMeasurements WHERE Unit=?",
        Parameters: [{S:"Grams"}],
        ConsistentRead: true,
    },
    ],
  }
}))
```
### Scan
```
await dbClient.query(JSON.stringify({
  operationType: 5,
  params:{
    TableName: "STRING_VALUE", // required
    IndexName: "STRING_VALUE",
    AttributesToGet: [ // AttributeNameList
      "STRING_VALUE",
    ],
    Limit: Number("int"),
    Select: "ALL_ATTRIBUTES" || "ALL_PROJECTED_ATTRIBUTES" || "SPECIFIC_ATTRIBUTES" || "COUNT",
    ScanFilter: { // FilterConditionMap
      "<keys>": { // Condition
        AttributeValueList: [ // AttributeValueList
        ],
        ComparisonOperator: "EQ" || "NE" || "IN" || "LE" || "LT" || "GE" || "GT" || "BETWEEN" || "NOT_NULL" || "NULL" || "CONTAINS" || "NOT_CONTAINS" || "BEGINS_WITH", // required
      },
    },
    ConditionalOperator: "AND" || "OR",
    ExclusiveStartKey: { // Key
      "<keys>": "<AttributeValue>",
    },
    ReturnConsumedCapacity: "INDEXES" || "TOTAL" || "NONE",
    TotalSegments: Number("int"),
    Segment: Number("int"),
    ProjectionExpression: "STRING_VALUE",
    FilterExpression: "STRING_VALUE",
    ExpressionAttributeNames: { // ExpressionAttributeNameMap
      "<keys>": "STRING_VALUE",
    },
    ExpressionAttributeValues: { // ExpressionAttributeValueMap
      "<keys>": "<AttributeValue>",
    },
    ConsistentRead: true || false,
  }
}))
```
For example:
```
ClientDynamo = DatabaseClient("ClientDynamo")
```
```
ClientDynamo.query(JSON.stringify({
  operationType: 5,
  params:{
    // Specify which items in the results are returned.
    FilterExpression: "Subtitle = :topic AND Season = :s AND Episode = :e",
    // Define the expression attribute value, which are substitutes for the values you want to compare.
    ExpressionAttributeValues: {
        ":topic": {S: "SubTitle2"},
        ":s": {N: 1},
        ":e": {N: 2},
    },
    // Set the projection expression, which are the attributes that you want.
    ProjectionExpression: "Season, Episode, Title, Subtitle",
    TableName: "EPISODES_TABLE",
  }
}))
```