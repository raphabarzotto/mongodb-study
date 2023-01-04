# Challenge 6
- Return snacks that got `between 10 and 100 likes`
- Show only `name` and `likes`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ curtidas: { $gt: 10, $lt: 100 } }, { _id: 0, nome: 1, curtidas: 1 });
  ```
</details>