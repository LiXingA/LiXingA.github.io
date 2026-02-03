<!--{"pinCode":false,"dname":"452ad6ee-90d8-4bb9-9773-8f7d777c387a","codeMode":"markdown"}-->
| <b>123</b> | dsfs |
| ---- | ---- |
| ewe | eeee |
| www | dddd |

<!--{"pinCode":true,"dname":"487a7be1-f2e9-47e9-b52c-1e4bab874e9b","codeMode":"markdown"}-->
| name   | quantity |
| ------ | -------- |
| apples | 12       |
| pears  | 34       |

<!--{"pinCode":false,"dname":"afb33211-9ce4-4657-9628-76361d3dccdc","codeMode":"markdown"}-->
<b>99999111111</b>

<!--{"pinCode":false,"dname":"bc149a7e-934a-4be6-b509-8e4b99c7fa53","codeMode":"markdown"}-->
123456

<!--{"pinCode":false,"dname":"a91f6a3b-431d-4772-8ec9-eb680ad82950","codeMode":"markdown"}-->
# bbb `ccc`

<!--{"pinCode":false,"dname":"2d56a15f-a3f7-47a5-b4a7-9721f15dd6c2","codeMode":"markdown"}-->
sfasfsd

<!--{"pinCode":false,"dname":"441496a1-4d50-470e-801f-d6872f6239aa","codeMode":"markdown"}-->
dfsfsdfsdf

<!--{"pinCode":false,"dname":"19b3a1b0-31f5-4b51-94ea-26f1e3e0283c","codeMode":"markdown"}-->
adsds	`cdeee` `code`

<!--{"pinCode":false,"dname":"03c461be-fc42-4a61-b70e-0369464468f8","codeMode":"markdown"}-->
# dddd

<!--{"pinCode":false,"dname":"32418f4e-8586-418f-9e11-420fb7eb0c2d","codeMode":"markdown"}-->
# `code` aaa

<!--{"pinCode":false,"dname":"c8677885-4aaa-428f-b116-b47d106ddbcb","codeMode":"markdown"}-->
# Untitled

<!--{"pinCode":false,"dname":"14bf6eb1-fb09-41d4-8638-5c9184c6fb35","codeMode":"markdown"}-->
# This

<!--{"pinCode":false,"dname":"c69f97cc-addd-4182-a426-ea6c62d97960","codeMode":"markdown"}-->
eweweewfd<i>afasdf</i>safdafw <code class="inline-code">wewewew</code>
aaaa

<!--{"pinCode":false,"dname":"c8ee8528-cedc-41b0-b3c8-10e020bb68ca","codeMode":"markdown"}-->
eweweewfd<i>afasdf</i>safdafw <code class="inline-code">wewewew</code>

<!--{"pinCode":false,"dname":"153ce455-31e2-4baa-be37-c88dca748f18","codeMode":"markdown"}-->
*   hkhkjkkhk
*   hkhj<code class="inline-code">kj jkljljjljkl</code> <code class="inline-code">jhhjkhjkk</code>
*   sdsdsddssd

<!--{"pinCode":false,"dname":"7395e121-f8fe-47ba-b5f4-3b50537ffc44","codeMode":"markdown"}-->
123456

<!--{"pinCode":false,"dname":"0ed52838-bd07-47ca-91bc-7ae767c051b3","codeMode":"markdown"}-->
aaaaa 222 `clode`

<!--{"pinCode":false,"dname":"1f821b11-15b8-4fbb-94b1-e0e7845484d6","codeMode":"markdown"}-->
# code dsdsd

<!--{"pinCode":false,"dname":"cd2c9b8e-e5e0-4128-b406-35b8c5f7bf4a","codeMode":"markdown"}-->
# Google Sheets Starter bbb

<!--{"pinCode":false,"dname":"bd4ecc5c-4f63-410c-ba0f-1fd7251d92b3","codeMode":"markdown"}-->
Paste a **shared** Google [Sheets URL below](https://duckduckgo.com "title(optional)") to fetch it as a CSV. This example shows undefined.

<!--{"pinCode":true,"dname":"6954aef3-e22f-46b0-a807-0f45a08ba230","codeMode":"js"}-->
```js
url = ("https://docs.google.com/spreadsheets/d/1ih4V4CumuIl5ZynobsazNzGiaPrE2V2Dpt13FI22XNU/edit#gid=0")
```

<!--{"pinCode":true,"dname":"2fe74060-c40d-4c3d-baaf-3d0801d6f6bf","codeMode":"js"}-->
```js
data = (d3.csv(getCsvUrl(url), d3.autoType))
```

<!--{"pinCode":true,"dname":"d03de98e-74dd-4415-abce-328e1cbabc38","codeMode":"js"}-->
```js
viewof table = Inputs.table(data)
```

<!--{"pinCode":false,"dname":"9cb7a333-b39b-4d43-9493-b103916c115a","codeMode":"markdown"}-->
***

<!--{"pinCode":true,"dname":"b8c1085c-23bb-4a2d-b297-8fa98a05584b","codeMode":"js"}-->
```js
getCsvUrl = (url => {
  url = new URL(url);
  const id = url.pathname.split("/")[3]
  const gid = new URLSearchParams(url.hash.slice(1)).get("gid") || 0;
  return `https://docs.google.com/spreadsheets/d/${id}/export?format=csv&gid=${gid}`
})
```
