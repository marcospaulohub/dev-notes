# 🔤 Tags HTML mais usadas

O HTML usa algo chamado modelo de caixa. A questão é que tudo no HTML é considerado uma **caixa dentro de outra caixa**

<div style="border: 5px solid black; padding: 20px; width: 400px; text-align:left;background-color: grey;">M
<div style="border: 5px solid black; padding: 4px; width: 350px; text-align:left;background-color: black;">B
    <div style="border: 5px solid black; padding: 10px; margin: 10px; width: 300px; text-align:left;background-color: green;">P
        <div style="border: 5px dashed  red; padding: 5px; margin-top: 1px;text-align:center;">C</div>
    </div>
</div>
</div>

* M - Magin
* B - Borda
* P - Padding
* C - Content

## `<span></span>`
O elemento `<span>` é usado para aplicar estilos a partes do texto.

```html
<p>Um exemplo de utilzação do span onde queremos enfatizar apenas 
<span> essa parte. </span>
</p>
```

## `<div></div>`
O elemento `<div>` é usado para agrupar e estilizar elementos.

Quando adicionamos um elemento `<div>` em torno de outros elementos, colocamos uma caixa maior em torno de outras caixas.

Porque o elemento `<div>` tem outros elementos aninhado dentro dele, nós o chamamos de elemento pai. O elemento `<p>` dentro dele é chamado de elemento filho.

```html
<body>
<div>
<p>Conteudo 1</p>
<p>Conteudo 2</p>
<p>Conteudo 3</p>
</div>
</body>
```

Quando estilizamos um elemento pai, existem algumas propriedades que afetam apenas o pai, como **border, padding, magin.**

```css
div {
	border: solid 3px lighGray;
}
```
Mas outras propriedades, como color, são transferidas para os elementos filhos a partir de seu pai. 
Exemplo de **color** como brown.

```css
div {
	border: solid 3px lighGray;
	color: brown;
}
```
Quando um elemento filho recebe uma propriedade de seu pai, chamamos isso de herança.



## Listas
`<ul>` e `<ol>` são tags HTML para criar listas.`<ul>` cria uma lista não ordenada (com marcadores), enquanto `<ol>` cria uma lista ordenada (numerada). Ambas as tags envolvem os itens da lista, que são definidos pela tag `<li>` (list item).

## Listas desordenadas (`<ul>`)
- Usada para agrupar itens que não têm uma ordem de importância ou sequência específica.
- Geralmente exibida com marcadores (pontos).

Exemplos :
```html
<ul>
  <li>Maçã</li>
  <li>Banana</li>
  <li>Laranja</li>
</ul>
```

Resultado :
- Maçã
- Banana
- Laranaja

## Listas ordenadas (`<ol>`)
- Usada para agrupar itens que devem seguir uma ordem específica, como um passo a passo.
- Geralmente exibida com números ou letras.

Exemplos :
```html
<ol>
  <li>Ligue o computador.</li>
  <li>Abra o navegador.</li>
  <li>Acesse o site.</li>
</ol>
```

Resultado :
  1. Ligue o computador.
  2. Abra o navegador.
  3. Acesse o site.

  ## Listas desordenadas (`<ul>`) dentro de Listas ordenadas (`<ol>`)

  É possível colocar uma `<ul>` dentro de uma `<ol>` para criar uma sublista não ordenada dentro de uma lista ordenada. O código HTML deve ter a `<ol>` como a lista principal, com os itens `<li>` que contêm outra `<ul>` para a sublista. 

Exemplos :

```html
<ol>
  <li>Item principal 1</li>
  <li>
    Item principal 2
    <ul>
      <li>Subitem 2.1</li>
      <li>Subitem 2.2</li>
    </ul>
  </li>
  <li>Item principal 3</li>
</ol>
```

**Como funciona**

- **`<ol>`:** Define a lista ordenada principal. Os itens da lista serão numerados.
- **`<li>`:** Representa cada item da lista. É um item `<li>` que contém a sublista.
- **`<ul>`:** Define a sublista não ordenada dentro de um item `<li>` da lista principal.

Resultado:

1. Item principal 1
2. Item principal 2
    - Subitem 2.1
    - Subitem 2.2
3. Item principal 3