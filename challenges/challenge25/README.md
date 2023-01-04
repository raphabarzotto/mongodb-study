# Challenge 25
- Add value `a lot of sodium` in tags of snacks that have more than `40% sodium percentage` in `nutritionalValues`
- Return all snacks
- Show only `name` and `tags`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany(
      { valoresNutricionais: { $elemMatch: { tipo: "sódio", percentual: { $gte: 40 } } } },
      { $push: { tags: "muito sódio" } },
    );

  db.produtos
    .find({}, { nome: 1, tags: 1, _id: 0 });
  ```
</details>