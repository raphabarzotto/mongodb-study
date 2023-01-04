# Challenge 9
- Return snacks with `protein percentage beetwen 30 and 40`
- Show only `name`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ "valoresNutricionais.3.percentual": { $gte: 30, $lte: 40 } }, { nome: 1, _id: 0 });
  ```
</details>