# Challenge 9
- Return snacks with `less than 500 calories`
- Show only `name`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ "valoresNutricionais.0.quantidade": { $lt: 500 } }, { _id: 0, nome: 1 });
  ```
</details>