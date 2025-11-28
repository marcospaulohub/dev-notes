# 🔧 Clone de Objetos no JavaScript
```js
let pessoa = {
    nome: 'Marcos Paulo',
    idade: 42
}

//Método do Objeto JSON que converte um Objeto em String
JSON.stringify(pessoa)

//Método do Objeto JSON que converte uma String em Objeto
JSON.parse("{nome: 'Marcos Paulo', idade:42}");

//Uma forma de clonar um objeto
let outraPessoa = JSON.parse(JSON.stringify(pessoa));

//OBS: Essa forma não resolve todos os casos. 
//A situações que o objeto tem prototype e essa forma não resolve. 
```