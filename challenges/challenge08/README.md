# Challenge 8
- Delete snacks with `less than 50 likes`
- Return remaining snacks

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .deleteMany({ curtidas: { $lt: 50 } });

  db.produtos
    .find({}, { _id: 0, nome: 1 });
  ```
</details>