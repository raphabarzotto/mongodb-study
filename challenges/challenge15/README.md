# Challenge 15
- Add `rating` to all documents
  - value equal to `5` to all document that have `bovino` tag
  - value equal to `3` to all document that have `ave` tag
  - value equal to `0` to the rest
- Return all documents
- Show only `name` and `rating`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany({}, { $set: { avaliacao: 0 } });

  db.produtos
    .updateMany({ tags: { $all: ["bovino"] } }, { $inc: { avaliacao: 5 } });

  db.produtos
    .updateMany({ tags: { $all: ["ave"] } }, { $inc: { avaliacao: 3 } });

  db.produtos
    .find({}, { _id: 0, nome: 1, avaliacao: 1 });
  ```
</details>