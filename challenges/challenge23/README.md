# Challenge 23
- Add values `combo` and `tasty` to all `tags`
- Order all tags by alphabetical order
- Return all snacks
- Show only `name` and `tags`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $push: { tags: { $each: ["combo", "tasty"], $sort: 1 } } });

  db.produtos
    .find({}, { nome: 1, tags: 1, _id: 0 });
  ```
</details>