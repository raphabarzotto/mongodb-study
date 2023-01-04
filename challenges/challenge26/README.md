# Challenge 26
- Add value `has sodium` in tags of snacks that have between than `20 and 40 sodium percentage` in `nutritionalValues`
- Return all snacks
- Show only `name` and `tags`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany(
      { valoresNutricionais: { $elemMatch: {
        tipo: "sódio",
        percentual: { $gt: 20, $lt: 40 },
      } } },
      { $push: { tags: "contém sódio" } },
    );

  db.produtos
    .find({}, { nome: 1, tags: 1, _id: 0 });
  ```
</details>