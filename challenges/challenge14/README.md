# Challenge 14
- Return all documents than have `picles` in `ingredients`
- Show only `name`, `ingredients` and the first 3 itens in `nutritionalValues`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find(
      { ingredientes: { $elemMatch: { $eq: "picles" } } },
      { _id: 0, nome: 1, ingredientes: 1, valoresNutricionais: { $slice: 3 } },
    );
  ```
</details>