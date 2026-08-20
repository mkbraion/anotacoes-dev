# JavaScript — snippets úteis

## Array methods que uso sempre
```js
const nums = [1, 2, 3, 4];

nums.map(n => n * 2);          // [2, 4, 6, 8]
nums.filter(n => n % 2 === 0); // [2, 4]
nums.reduce((acc, n) => acc + n, 0); // 10
```

## async/await
```js
async function buscarUsuario(id) {
  try {
    const res = await fetch(`/api/users/${id}`);
    if (!res.ok) throw new Error("Falha na requisição");
    return await res.json();
  } catch (e) {
    console.error(e);
    return null;
  }
}
```

## Formatar dinheiro em BRL
```js
const brl = (v) =>
  v.toLocaleString("pt-BR", { style: "currency", currency: "BRL" });

brl(1234.5); // "R$ 1.234,50"
```
