# Challenge 24
- Order in all documents in `nutritionalValues` by descending order based on `percentage`
- Return all snacks
- Show only `name` and `nutritionalValues`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $push: { valoresNutricionais: { $each: [], $sort: { percentual: -1 } } } });

  db.produtos
    .find({}, { nome: 1, valoresNutricionais: 1, _id: 0 });
  ```
</details>