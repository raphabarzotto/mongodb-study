# Challenge 7
- Return snacks that sold a number `different than 50` and got no `tags`
- Show only `name` and `quantity`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos.find(
    { $and: [{ vendidos: { $ne: 50 } }, { tags: { $exists: false } }] },
    { _id: 0, nome: 1, vendidos: 1 },
  );
  ```
</details>