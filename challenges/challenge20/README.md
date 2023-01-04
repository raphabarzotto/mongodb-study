# Challenge 20
- Remove first `ingredient` from snack named `Quarteirão com Queijo`
- Return all snacks
- Show only `name` and `ingredients`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateOne({ nome: "Quarteirão com Queijo" }, { $pop: { ingredientes: -1 } });

  db.produtos
    .find({}, { _id: 0, nome: 1, ingredientes: 1 });
  ```
</details>