# Challenge 27
- Count how many products has `Mc`
- Ignore lower and upper cases

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .countDocuments({ nome: { $regex: /Mc/i } });
  ```
</details>