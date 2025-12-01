# 📚 Principais Métodos
Os principais métodos do objeto **document** do HTML, que faz parte do **Document Object Model (DOM)**,  são usados para acessar e manipular os elementos da página com JavaScript.

## Métodos para encontrar elementos

- `document.getElementById(id)`: Retorna o elemento com o atributo `id` especificado.
- `document.getElementsByClassName(nomeDaClasse)`: Retorna uma coleção de elementos com o nome de classe especificado.
- `document.getElementsByTagName(nomeDaTag)`: Retorna uma coleção de elementos com o nome da tag especificada, como `<div>`, `<p>`, `<a>`.
- `document.querySelector(seletorCSS)`: Retorna o **primeiro** elemento que corresponde ao seletor CSS especificado.
- `document.querySelectorAll(seletorCSS)`: Retorna uma lista de **todos** os elementos que correspondem ao seletor CSS especificado.

## Métodos para manipular o conteúdo

- `document.createElement(nomeDaTag)`: Cria um novo elemento HTML com o nome da tag especificada.
- `document.createTextNode(texto)`: Cria um novo nó de texto.
- `elemento.appendChild(novoNo)`: Adiciona um novo nó como o último filho de um elemento.
- `elemento.innerHTML`: Obtém ou define o conteúdo HTML (incluindo tags) de um elemento.
- `elemento.innerText`: Obtém ou define o conteúdo de texto de um elemento, sem incluir tags.