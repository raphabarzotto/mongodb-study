# Challenge 21
- Remove last `ingredient` from snack named `Cheddar McMelt`
- Return all snacks
- Show only `name` and `ingredients`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateOne({ nome: "Cheddar McMelt" }, { $pop: { ingredientes: 1 } });

  db.produtos
    .find({}, { _id: 0, nome: 1, ingredientes: 1 });
  ```
</details>