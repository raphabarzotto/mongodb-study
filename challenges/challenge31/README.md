# Challenge 31
- Return all documents that `likes` is greater than `quantity`
- Show only `name`


<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ $expr: { $gt: ["$curtidas", "$vendidos"] } }, { _id: 0, nome: 1 });
  ```
</details>