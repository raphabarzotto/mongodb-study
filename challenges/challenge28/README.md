# Challenge 28
- Count how many products has exactly `4` ingredients

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .count({ ingredientes: { $size: 4 } });
  ```
</details>