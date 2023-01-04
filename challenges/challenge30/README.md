# Challenge 30
- Remove `likes` field of `Big Mac` item
- Return all documents
- Show only `name` and `likes`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateOne({ nome: "Big Mac" }, { $unset: { curtidas: "" } });

  db.produtos
    .find({}, { _id: 0, nome: 1, curtidas: 1 });
  ```
</details>