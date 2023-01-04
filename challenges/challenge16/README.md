# Challenge 16
- Add `lastChange` to `Big Mac`
- Return this document

<details>
  <summary><strong>Answer</strong></summary>

  ```js
  db.produtos
    .updateOne({ nome: "Big Mac" }, { $currentDate: { ultimaModificacao: true } });

  db.produtos
    .find({ ultimaModificacao: { $exists: true } }, { _id: 0, nome: 1 }); 
  ```
</details>