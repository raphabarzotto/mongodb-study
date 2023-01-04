# Challenge 29
- Rename `descricao` field to `descrisaoSite` in all documents
- Return all documents
- Show only `name` and `descrisaoSite`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $rename: { descricao: "descricaoSite" } });

  db.produtos
    .find({}, { _id: 0, nome: 1, descricaoSite: 1 });
  ```
</details>