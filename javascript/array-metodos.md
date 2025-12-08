# 📚 Métodos e atributos de um Array

Em JavaScript, um array é um objeto especial que armazena uma lista ordenada de valores. Ele possui diversos atributos (propriedades) e métodos nativos que facilitam o trabalho com coleções de dados.

Abaixo estão os principais atributos e métodos que você precisa conhecer:

## ✅ Principais atributos (propriedades) de um Array

`length`
* Retorna o número de elementos do array.
```js
const frutas = ["maçã", "banana", "uva"];
console.log(frutas.length); // 3
``` 

**Índices numéricos**
* Cada elemento pode ser acessado diretamente pelo seu índice:
```js
frutas[0]; // "maçã"
frutas[2]; // "uva"
``` 
---

## ✅ Principais métodos de um Array

### ➕ Adição
`push()`
* Adiciona um elemento no final do array.
```js
frutas.push("laranja");
``` 

`unshift()`
* Adiciona elemento no início.
```js
frutas.unshift("mamão");
``` 
Podemos adicionar múltiplos valores separando-os com uma vírgula `,`.
```js
frutas.push("tangerina", "pera"); // vai para o final do array.
frutas.unshift("banana","goiaba"); // vai para o inicio do array.
```

Os métodos `push()` ou `unshift()` retornam o valor total de elementos do array após a adição.

```js
const frutas = ["maça","laranja", "pera"];

let totalFrutas = frutas.push("uva");
console.log(totalFrutas);//4

totalFrutas = frutas.unshift("tangerina");
console.log(totalFrutas);//5
``` 






---

### ➖ Remoção
`pop()`
* Remove o último elemento.
```js
frutas.pop();
``` 

`shift()`
* Remove o primeiro elemento.
```js
frutas.shift();
``` 
Podemos atribuir a uma variável o elemento que estamos removendo.

```js
const frutas = ["maça","laranja","limão","tangerina"];

let ultimaFruta = frutas.pop();
console.log(ultimaFruta); // tangerina

let primeiraFruta = frutas.shift();
console.log(primeiraFruta); // maça
``` 
--- 

### 🔎 Procurar valores

`indexOf()`
* Retorna o índice da primeira ocorrência.
```js
frutas.indexOf("laranja"); // 1
``` 

`includes()`
* Verifica se um valor existe.
```js
frutas.includes("limão"); // true
``` 
---

### ➡️Ordenação e ⬅️Reversão
`sort()`
* Ordena o array.
```js
const numeros = [3, 1, 2];
numeros.sort(); // [1, 2, 3]
``` 
⚠️ Para números reais é melhor usar:
```js
numeros.sort((a, b) => a - b);
``` 

`reverse()`
* Inverte a ordem dos elementos.
```js
numeros.reverse();
numeros.sort(); // [3, 2, 1]
``` 
