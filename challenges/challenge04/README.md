# Challenge 4
- Return snacks that sold more than 50 and less than 100
- Show only `name` and `quantity`
- Order by `quantity`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({ vendidos: { $gt: 50, $lt: 100 } }, { _id: 0, nome: 1, vendidos: 1 })
    .sort({ vendidos: 1 });
  ```
</details>