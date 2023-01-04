# Challenge 19
- Remove `cebola` from all `ingredients`
- Return all snacks
- Show only `name` and `ingredients`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $pull: { ingredientes: "cebola" } });

  db.produtos
    .find({}, { _id: 0, nome: 1, ingredientes: 1 });
  ```
</details>