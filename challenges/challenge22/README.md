# Challenge 22
- Add `salesByDay` field in all documents
  - Start value will be: `[0, 0, 0, 0, 0, 0, 0]`
  - First item in array is Sunday sales
  - Increment Wednesday `Big Mac` Sales by 60
  - Increment by 120 all Saturday sales from snacks that have `bovino` tag
- Return all snacks
- Show only `name` and `salesByDay`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $set: { vendasPorDia: [0, 0, 0, 0, 0, 0, 0] } });

  db.produtos
    .updateOne({ nome: "Big Mac" }, { $inc: { "vendasPorDia.3": 60 } });
    
  db.produtos
    .updateMany({ tags: "bovino" }, { $inc: { "vendasPorDia.6": 120 } });
    
  db.produtos
    .find({}, { _id: 0, nome: 1, vendasPorDia: 1 });
  ```
</details>