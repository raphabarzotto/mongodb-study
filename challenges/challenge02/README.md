# Challenge 2
- Order `produtos` collection by quantity of sold snacks
- Show only `name` and `quantity`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({}, { _id: 0, nome: 1, vendidos: 1 })
    .sort({ vendidos: 1 });
  ```
</details>