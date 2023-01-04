# Challenge 5
- Return snacks that got exactly `36 likes` or `85 sales`
- Show only `name`, `like` and `quantity`

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