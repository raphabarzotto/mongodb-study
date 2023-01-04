# Challenge 6
- Return snacks that got `between 10 and 100 likes`
- Show only `name` and `likes`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos.find({
    $or: [
      { curtidas: { $eq: 36 } },
      { vendidos: { $eq: 85 } },
    ],
  }, { _id: 0, nome: 1, curtidas: 1, vendidos: 1 });
  ```
</details>