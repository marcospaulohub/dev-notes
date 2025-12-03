# 🚀 Map, Filter e Reduce em JavaScript

## 📌 1. `map()`

### O que faz?

Cria **um novo array** com o resultado da função aplicada a **cada
item** do array original.

### Quando usar?

-   Quando você quer **transformar** os valores de um array.

### Exemplo simples

#### 👉 Transformando números

``` js
const numeros = [1, 2, 3, 4, 5];

const dobrados = numeros.map(num => num * 2);

console.log(dobrados); 
// Resultado: [2, 4, 6, 8, 10]
```

#### 👉 Trabalhando com objetos

``` js
const pessoas = [
  { nome: "Ana", idade: 18 },
  { nome: "João", idade: 22 },
  { nome: "Pedro", idade: 30 }
];

const nomes = pessoas.map(p => p.nome);

console.log(nomes); 
// Resultado: ["Ana", "João", "Pedro"]
```

------------------------------------------------------------------------

## 📌 2. `filter()`

### O que faz?

Cria **um novo array** com os itens **que passam em uma condição**.

### Quando usar?

-   Quando você quer **selecionar** elementos de um array.

### Exemplo simples

#### 👉 Filtrando números maiores que 10

``` js
const numeros = [5, 12, 8, 130, 44];

const maiores = numeros.filter(num => num > 10);

console.log(maiores);
// Resultado: [12, 130, 44]
```

#### 👉 Filtrando objetos

``` js
const produtos = [
  { nome: "TV", preco: 2500 },
  { nome: "Celular", preco: 1500 },
  { nome: "Mouse", preco: 80 }
];

const caros = produtos.filter(prod => prod.preco > 1000);

console.log(caros);
// Resultado: [{ nome: "TV", preco: 2500 }, { nome: "Celular", preco: 1500 }]
```

------------------------------------------------------------------------

## 📌 3. `reduce()`

### O que faz?

**Reduz** um array a **um único valor**, acumulando resultados.

### Quando usar?

-   Somar, contar, agrupar, calcular algo baseado em todos os itens do
    array.

### Exemplo simples

#### 👉 Somando valores

``` js
const numeros = [1, 2, 3, 4, 5];

const soma = numeros.reduce((acumulador, valorAtual) => acumulador + valorAtual, 0);

console.log(soma);
// Resultado: 15
```

#### 👉 Somando preços

``` js
const compras = [
  { item: "Arroz", preco: 12 },
  { item: "Carne", preco: 35 },
  { item: "Suco", preco: 8 }
];

const total = compras.reduce((acc, prod) => acc + prod.preco, 0);

console.log(total);
// Resultado: 55
```

------------------------------------------------------------------------

## 🎯 Exemplo combinando os três

``` js
const numeros = [4, 6, 8, 10];

const resultado = numeros
  .map(n => n * 2)         // [8, 12, 16, 20]
  .filter(n => n > 10)     // [12, 16, 20]
  .reduce((acc, n) => acc + n, 0); // 48

console.log(resultado);
// Resultado: 48
```

------------------------------------------------------------------------

## ✍️ Resumão
| Método      | Retorna                  | Usado para |
| --------    | -----                    | ----------- |
| **map**     | novo array transformado  | transformação de valores.|
| **filter**  | novo array filtrado      | seleção com condição.|
| **reduce**  | valor único              | somar, agrupar e acumular.|
