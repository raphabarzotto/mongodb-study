# Challenge 13
- Add `createdBy` in all documents with value `Ronald McDonald`
- Return all snacks
- Show only `name` and `createdBy`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $set: { criadoPor: "Ronald McDonald" } });

  db.produtos
    .find({}, { _id: 0, nome: 1, criadoPor: 1 });
  ```
</details>