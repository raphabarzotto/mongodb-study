# Challenge 12
- Add `ketchup` in `ingredients`
- Name different than `McChicken`
- Should not have ingredient duplicity
- Return all snacks
- Show only `name` and `ingredients`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateMany(
      { nome: { $ne: "McChicken" } },
      { $addToSet: { ingredientes: "ketchup" } },
    );

  db.produtos
    .find({}, { _id: 0, nome: 1, ingredientes: 1 });
  ```
</details>