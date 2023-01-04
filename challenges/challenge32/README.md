# Challenge 32
- Return all documents that `quantity` is a multiple of `5`
- Show only `name` and `quantity`


<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ $expr: { $gt: ["$curtidas", "$vendidos"] } }, { _id: 0, nome: 1 });
  ```
</details>