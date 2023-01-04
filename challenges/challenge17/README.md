# Challenge 17
- Create a new collection `resumoProdutos`
- Create `franchise` field with value `McDonalds`
- Create `totalProducts` field with count of documents in `produtos` collection
- Return this

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.resumoProdutos
    .insert({ franquia: "McDonalds", totalProdutos: db.produtos.countDocuments({}) });

  db.resumoProdutos
    .find({}, { _id: 0, franquia: 1, totalProdutos: 1 });
  ```
</details>