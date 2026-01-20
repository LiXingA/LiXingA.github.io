<!--{"type":"header","level":1}-->
# Mutable, reactive counter

<!--{"type":"paragraph"}-->
Click the buttons to update a mutable value and see dependent cells react immediately.

<!--{"pinCode":false,"dname":"b5a5f5c6-2b3b-4b9f-bf2f-51a0b1a9f3a2","codeMode":"js"}-->
```js
mutable count = 0
```

<!--{"pinCode":false,"dname":"2c2d3a8a-5c9c-4a2b-9f0d-2b0c56a3f8ef","codeMode":"js"}-->
```js
viewof controls = {
  const root = html`<div style="display:flex; gap:8px; align-items:center;">
    <button>–</button>
    <button>+</button>
    <button>Reset</button>
  </div>`;

  const [dec, inc, reset] = root.querySelectorAll("button");

  dec.addEventListener("click", () => (mutable count = count - 1));
  inc.addEventListener("click", () => (mutable count = count + 1));
  reset.addEventListener("click", () => (mutable count = 0));

  return root;
}
```

<!--{"pinCode":false,"dname":"0e2a1a79-1b59-4c56-9c8a-9c4d5f8b3b2c","codeMode":"js"}-->
```js
count
```

<!--{"pinCode":false,"dname":"c225235c-e581-4996-8b2c-210890f6f035","codeMode":"markdown"}-->
**Squared:** ${count \\* count}
