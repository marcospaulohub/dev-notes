# 📦 Objetos em JavaScript

```js
let pessoa = {
    nome: 'Marcos Paulo',
    idade: 42
}

//Exibir 
console.log(pessoa);
{nome: 'Marcos Paulo', idade:42}

//Adicionando um campo
pessoa.profissao = 'Desenvolvedor'
//ou
pessoa[profissao] = 'Desenvolvedor'

//Exibir
console.log(pessoa);
{nome: 'Marcos Paulo', idade:42, profissao:'Desenvolvedor'}

//Removendo um campo
delete.pessoa.profissao

//Adicionando um Array
pessoa.hobbies = ['Programar','Jogar']

//Exibir
console.log(pessoa);
{nome: 'Marcos Paulo', idade: 42, profissao: 'Desenvolvedor', hobbies: Array(2)}

//Adicionando um Objeto
pessoa.cachorro = {
    nome: 'bilu',
    idade: 2
}

//Exibir
console.log(pessoa);
{nome: 'Marcos Paulo', idade: 42, profissao: 'Desenvolvedor', hobbies: Array(2), cachorro: {…}}

```
