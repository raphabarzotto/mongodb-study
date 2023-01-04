# Challenge 18
- Update `Big Mac` and `Quateirão com Queijo` snacks with `bacon` in `ingredients` list
- Return all snacks
- Show only `name` and `ingredients`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany(
      { nome: { $in: ["Big Mac", "Quarteirão com Queijo"] } }, 
      { $push: { ingredientes: "bacon" } },
    );

  db.produtos
    .find({}, { _id: 0, nome: 1, ingredientes: 1 });
  ```
</details>