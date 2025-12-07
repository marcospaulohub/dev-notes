# 🧩 Guia Rápido de CSS

Este guia traz os principais conceitos, seletores, propriedades e exemplos práticos para consulta rápida.

---

## 📌 O que é CSS?
CSS (Cascading Style Sheets) é a linguagem usada para definir estilos para páginas HTML, como cores, fontes, tamanhos, espaçamento e posicionamento de elementos.

---

## 🧲 Formas de aplicar CSS

### ▶️ Inline
```css
<p style="color: red;">Texto vermelho</p>
```

### ▶️ Interno
```css
<style>
  p { color: red; }
</style>

```

### ▶️ Externo
```css
<link rel="stylesheet" href="styles.css">
```
---
### 🎯 Seletores principais
**Tipo**
```css
p { color: blue; }
```

**Classe**
```css
.box { border: 1px solid black; }
```

**ID**
```css
#titulo { font-size: 32px; }
```
**Agrupamento**
```css
h1, h2, p { margin: 0; }
```
**Descendente**
```css
ul li a { color: green; }
```
**Pseudo-classes**
```css
a:hover { color: red; }
input:focus { border-color: blue; }
```
**Pseudo-elementos**
```css
p::first-line { font-weight: bold; }
```
---
### 🎨 Cores
- HEX: `#3498db`
- RGB: `rgb(52, 152, 219)`
- RGBA: `rgba(52, 152, 219, .5)`
- HSL: `hsl(204, 70%, 53%)`

---

### ✍️ Fontes e textos
```css
body {
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;
  text-align: center;
  text-decoration: underline;
  text-transform: uppercase;
}
```
---
### 📦 Box Model
Todos os elementos possuem:

- `width`
- `height`
- `padding` (dentro)
- `border`
- `margin` (fora)
```css
div {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
}
``` 
---
### 📏 Unidade de medidas
- Absolutas: `px`, `pt`, `cm`
- Relativas: `em`, `rem`, `%`, `vh`, `vw`
---

### 🧱 Display
```css
.block { display: block; }
.inline { display: inline; }
.inline-block { display: inline-block; }
.flex { display: flex; }
.grid { display: grid; }
.none { display: none; }
``` 
---
### 🧭 Position
```css
.relative   { position: relative; }
.absolute   { position: absolute; }
.fixed      { position: fixed; }
.sticky     { position: sticky; }
``` 
Exemplo:
```css
.box {
  position: absolute;
  top: 20px;
  left: 30px;
}
``` 
---
### 🎛️ Flexbox (básico)
```css
.container {
  display: flex;
  justify-content: center;    /* eixo principal */
  align-items: center;        /* eixo cruzado */
  gap: 20px;
}
``` 
---
### 🧩 Grid (básico)
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
}
``` 
---
### 🌁 Backgrounds
```css
body {
  background-color: #222;
  background-image: url('img/bg.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
``` 
---
### 🪄 Transições e animações
**Transição**
```css
button {
  background: blue;
  transition: background .3s;
}

button:hover {
  background: red;
}
``` 
**Animação**
```css
@keyframes mover {
  from { left: 0; }
  to { left: 200px; }
}

.box {
  position: relative;
  animation: mover 2s infinite alternate;
}
``` 
---

### 🔐 Importante: Especificidade
Prioridade de CSS (do menor para o maior):

1. seletor de tipo (`p`)
2. classe (`.box`)
3. id (`#titulo`)
4. inline (`style="..."`)
5. `!important` (evite!!)
---

### 🧼 Reset básico
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
``` 
---

### 🧰 Dicas úteis
- Use `devtools` do navegador (F12)
- Use variáveis CSS:
```css
:root {
  --cor-principal: #3498db;
}

h1 {
  color: var(--cor-principal);
}
``` 
- Organize o CSS por seções
- Prefira classes ao invés de IDs
--- 

### 📚 Recursos recomendados
- MDN Web Docs (Mozilla)
- CSS Tricks
- W3Schools
- Flexbox Froggy
- Grid Garden
---







<!-- 
```css

``` 
-->
