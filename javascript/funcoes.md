# 🔧 Funções no JavaScript

### 1. Declaração de Função (Function Declaration)

Esta é a forma mais clássica. A principal característica aqui é o Hoisting (içamento), o que significa que você pode chamar a função antes de declará-la no código.
```js
function somar(a, b) {
  return a + b;
}

console.log(somar(2, 3)); // Saída: 5
```

### 2. Expressão de Função (Function Expression)

Aqui, a função é atribuída a uma variável. Diferente da anterior, esta função não sofre hoisting, ou seja, você só pode usá-la depois de declarar a variável.

```js
const subtrair = function(a, b) {
  return a - b;
};

console.log(subtrair(10, 5)); // Saída: 5
```
**Nota**: É comum ver essa forma sendo usada para passar funções como argumentos para outras funções (callbacks).

### 3. Arrow Function (Função de Seta)

Introduzida no ES6 (EcmaScript 2015), é a sintaxe mais moderna e concisa. Ela é muito usada hoje em dia, especialmente em programação funcional e frameworks como React.

**Sintaxe Padrão**:
```js
const multiplicar = (a, b) => {
  return a * b;
};
```

**Retorno Implícito (One-liner)**: Se a função tiver apenas uma linha de código, você pode omitir as chaves ```{}``` e a palavra ```return```.

```js
const multiplicar = (a, b) => a * b;
```

### 4. IIFE (Immediately Invoked Function Expression)
Esta é uma função que é declarada e **executada imediatamente**. Era muito usada antigamente para criar escopos privados e evitar poluir o escopo global.

```js
(function() {
  const mensagem = "Executei agora!";
  console.log(mensagem);
})();
```

### 5. Definição de Método (Method Definition)

Quando você está dentro de um Objeto ou de uma Classe, existe uma sintaxe curta para definir funções. Você não precisa da palavra-chave ```function``` nem dos dois pontos ```:```.

```js
const calculadora = {
  // Sintaxe curta (ES6)
  dividir(a, b) {
    return a / b;
  },
  
  // Sintaxe antiga (chave: valor)
  zerar: function() {
    console.log("Zerado");
  }
};
```

### 6. Função Construtora (Constructor Function)
Antes das ```Classes``` existirem no JavaScript, usávamos funções para criar "moldes" de objetos. Por convenção, começam com letra maiúscula.

```js
function Carro(marca, modelo) {
  this.marca = marca;
  this.modelo = modelo;
}

const meuCarro = new Carro("Toyota", "Corolla");
```

### Resumo Rápido


| Tipo            | Sintaxe Básica                | Principal Característica |
| --------        | -----                         | ----------- |
| **Declaration** | ```function x() {}```         | Sofre Hoisting (pode chamar antes de criar).|
| **Expression**  | ```const x = function() {}``` | Salva em variável, leitura sequencial.|
| **Arrow**       | ```const x = () => {}```      | Concisa, não tem seu próprio ```this```.|
| **IIFE**        | ```(function(){})()```        | Executa na hora, isola escopo.|



## Funções em Objetos
```js
//Forma 1
let calculadora = {
  soma: function(a, b) {
    return a + b;
  }
}

//Forma 2
let calculadora = {
  soma(a, b) {
    return a + b;
  }
}

//Forma 3 - Arrow function
let calculadora = {
  soma: (a, b) => a + b
}

//Várias funções no objeto
let calculadora = {
  soma: (a, b) => a + b,
  divisao: (a, b) => a / b,
  multiplicacao: (a, b) => a * b
}

```