# Challenge 3
- Show most sold snack
- Show only `name` and `quantity`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find({}, { _id: 0, nome: 1, vendidos: 1 })
    .sort({ vendidos: -1 })
    .limit(1);
  ```
</details>