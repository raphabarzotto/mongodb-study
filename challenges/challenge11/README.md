# Challenge 11
- Return all products
- Name different than `Big Mac` and `McChicken`
- Show only `name`, `likes` and `quantity`

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .find(
      { nome: { $nin: ["Big Mac", "McChicken"] } },
      { _id: 0, nome: 1, curtidas: 1, vendidos: 1 },
    );
  ```
</details>