<!--{"pinCode":true,"dname":"c81dd1d1-b99d-443c-ae62-91bd37ecc797","codeMode":"js"}-->
```js
app = render(({ useSetter }) => {
    const { Space } = Antd;
    return jsx`<${Space} key='c676a521-8579-4327-a4dd-810e709c7d42' direction="vertical">
    text
    </${Space}>`;
})
```

<!--{"blockType":"paragraph"}-->
888888888888888885555555544444455555588888866

<!--{"blockType":"paragraph"}-->
![1 (4).jfif](files/1 (4).jfif "1 (4).jfif")

<!--{"blockType":"header"}-->
## 554588899999999999900000055

<!--{"blockType":"list"}-->
*   5555
    *   pppp
    *   3333
<!--{"blockType":"warning","attr":{"title":"ddd"}}-->
> [!WARNING]
> wwwssss

<!--{"pinCode":false,"dname":"916e846b-105e-4d4e-ac73-37224abe68c1","codeMode":"markdown"}-->
```md
## kuzu api
```

<!--{"pinCode":true,"dname":"aebd88b8-9ed3-43d8-a255-9306700b2313","codeMode":"js"}-->
```js
viewof button_6 = Inputs.button("Fetch",{reduce:async ()=>{
  return await (await commonFetch(`/graphxr/api/kuzu/query/${projectId}/default?query=match(n)-[r]-(m) return *`)).json()
        }})
```

<!--{"pinCode":true,"dname":"7f6a7f57-4ea2-441a-abc8-1b7fbade0abb","codeMode":"js"}-->
```js
button_6
```

<!--{"pinCode":true,"dname":"c07deda9-67ca-449d-bba5-a3f14a59d4fe","codeMode":"js"}-->
```js
viewof button_7 = Inputs.button("POST",{
  reduce:async () => { 
    return await fetch(`/graphxr/api/kuzu/query/${projectId}/default`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({
        query: 'match(n)-[r]-(m) return * limit $limit',
        parameters:{
          limit: 2
        }
      })
    })
      .then(response => response.json())
      .then(data => data?.content)
      .catch(error => error);

  }
})
```

<!--{"pinCode":true,"dname":"99807436-5628-40c5-93a0-fec7c7094e6a","codeMode":"js"}-->
```js
button_7
```

<!--{"pinCode":true,"dname":"cfd09cb6-287d-49d8-bb43-23aae537e926","codeMode":"js"}-->
```js
commonFetch = function (resource, ...args) {
  return fetch(prefixAliasPath(resource), ...args);
}
```

<!--{"pinCode":true,"dname":"9a02e028-0363-417f-9b67-6a6e5dea5590","codeMode":"js"}-->
```js
window.groveConfig
```

<!--{"pinCode":true,"dname":"d9354528-cc38-4f2b-92ed-76f6ad60936a","codeMode":"js"}-->
```js
GROVE_HELP_URL = "https://grove-help.graphxr.com/";
```

<!--{"pinCode":true,"dname":"bf11868e-d9bd-465e-9f01-244e4f1f036a","codeMode":"js"}-->
```js
prefixAliasPath = function (path) {
    if (!path) {
      return path;
    }
    if (path.startsWith("blob:")) {
      return path;
    }
    if ((window.groveConfig?.noOnlineRequire) && path.startsWith(GROVE_HELP_URL)) {
      path = path.replace(GROVE_HELP_URL, window.GUIDE_LINK_URI);
    }
    if (!ALIAS_PATH) return path
    if (!path.startsWith('/')) return path;
    if (path.startsWith(ALIAS_PATH)) return path
    return ALIAS_PATH + path;
  }
```

<!--{"pinCode":true,"dname":"1efa1930-2f81-48e5-b442-51833460155c","codeMode":"js"}-->
```js
ALIAS_PATH = OPENER.globalVariable.aliasPath ?? '';
```

<!--{"pinCode":true,"dname":"af9dc4b6-fbe0-44ca-9704-16c1f11a5f33","codeMode":"js"}-->
```js
OPENER = window?.parent?.globalVariable ? window.parent : window.opener;
```

<!--{"pinCode":true,"dname":"da275ba6-b862-4ce5-80fc-261ffd67e2c8","codeMode":"js"}-->
```js
projectId = OPENER.globalVariable.project._id
```

<!--{"pinCode":true,"dname":"9a500864-b6af-4af9-852f-45fe7bb96056","codeMode":"js"}-->
```js
kuzuId = 'default'
```

<!--{"pinCode":false,"dname":"01147c31-a096-4ff0-acba-d64b0bf7a91d","codeMode":"js"}-->
```js
viewof button_5 = Inputs.button("drop database kuzuDBName",{reduce:async ()=>{
           return await gxr.query(`drop database kuzuDBName`)
        }})
```

<!--{"pinCode":false,"dname":"b365c2bf-57eb-45af-8444-adf8b025017d","codeMode":"js"}-->
```js
viewof button_4 = Inputs.button("create database kuzuDBName",{reduce:async ()=>{
           return await gxr.query(`create database kuzuDBName`)
        }})
```

<!--{"pinCode":false,"dname":"60394600-34b5-4d26-96e9-759e35085512","codeMode":"js"}-->
```js
button_4
```

<!--{"pinCode":false,"dname":"e90260dd-922c-4a0a-baf6-6f91f6ede542","codeMode":"js"}-->
```js
viewof button_3 = Inputs.button("show databases",{reduce:async ()=>{
           return await gxr.query(`show databases`)
        }})
```

<!--{"pinCode":false,"dname":"150099cc-f554-4f3e-b5bd-d96e96f906a8","codeMode":"js"}-->
```js
button_3
```

<!--{"pinCode":false,"dname":"1b5ddfe3-c7b9-49fa-85f8-b85d3d0019eb","codeMode":"js"}-->
```js
viewof button_2 = Inputs.button("CALL demo",{reduce:async ()=>{
           return await gxr.query(`CALL demo`)
        }})
```

<!--{"pinCode":false,"dname":"24ccb552-a3cf-4c80-a3c7-c9e9f28bb644","codeMode":"js"}-->
```js
button_2
```

<!--{"pinCode":false,"dname":"2e304ad8-0317-4625-8456-88a4e6986731","codeMode":"js"}-->
```js
viewof button_1 = Inputs.button("CALL reset",{reduce:async ()=>{
           return await gxr.query(`CALL reset`)
        }})
```

<!--{"pinCode":false,"dname":"9c56642a-1a39-4654-9755-e2b150cabeb4","codeMode":"js"}-->
```js
button_1
```

<!--{"pinCode":false,"dname":"78a2916d-c286-49cb-bc36-cc5850610dd5","codeMode":"jsx"}-->
```jsx
viewof button = render(({ useSetter }) => {
    const { Button } = Antd;
    const [step_number, setStep_number] = useState(1);
    const update_step_number =  async(d) => {
      // Create the tables
      await gxr.query(`CALL reset();
    CREATE NODE TABLE IF NOT EXISTS User(name STRING, age INT64, PRIMARY KEY (name));
    CREATE NODE TABLE IF NOT EXISTS City(name STRING, population INT64, PRIMARY KEY (name));
    CREATE REL TABLE IF NOT EXISTS Follows(FROM User TO User, since INT64);
    CREATE REL TABLE IF NOT EXISTS LivesIn(FROM User TO City);
    COPY User From "https://alt.graphxr.kinevizlabs.com/public/data/social-network/user.csv" (HEADER=true, IGNORE_ERRORS=true);
    COPY City FROM "https://alt.graphxr.kinevizlabs.com/public/data/social-network/city.csv" (HEADER=true, IGNORE_ERRORS=true);
    COPY Follows FROM "https://alt.graphxr.kinevizlabs.com/public/data/social-network/follows.csv" (HEADER=true, IGNORE_ERRORS=true);
    COPY LivesIn FROM "https://alt.graphxr.kinevizlabs.com/public/data/social-network/lives-in.csv" (HEADER=true, IGNORE_ERRORS=true);
    MATCH (u)-[r]->(m)
    RETURN u, r, m LIMIT 10;`);
    };
    useSetter({ step_number });
    return <Button key='6756d79f-6be3-4e39-89d7-90ac01d8b81b' onClick={update_step_number}  >Init Graph</Button> ;
})
```

<!--{"pinCode":false,"dname":"465cb402-b7fb-47c8-b1b5-398aefe788c7","codeMode":"js"}-->
```js
// test = gxr.query("MATCH (a:User)-[f:Follows]->(b:User) RETURN a.name, f.since, b.name;");
```

<!--{"pinCode":false,"dname":"8255339b-2697-4386-888e-9d0d31098d67","codeMode":"js"}-->
```js
import {jsx, render, useState, component, useEffect, Fragment } from "https://grove-help.graphxr.com/react/react"
```

<!--{"pinCode":true,"dname":"235ae951-e67b-4a76-86c7-37e538aceaa0","codeMode":"js"}-->
```js
// gxr.query('MATCH (n) RETURN n limit 10;', { type: "localKuzuFile", name:  "example.kuzu", saveToGraph: true})
```
