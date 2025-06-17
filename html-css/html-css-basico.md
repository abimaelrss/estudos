# Fundamentos HTML e CSS

Esse arquivo contém os principais fundamentos de HTML (HyperText Markup Language), a linguagem responsável por estruturar o conteúdo da web, e fundamentos do CSS — a linguagem usada para estilizar páginas web. Os conceitos aqui apresentados são essenciais para qualquer desenvolvedor front-end.

---

## HTML

### Primeiros passos

- **O que é HTML?**
  HTML é a linguagem de marcação utilizada para criar páginas na web. Ele define a estrutura do conteúdo usando **tags**.

- **Comentários no HTML**
  São trechos que o navegador ignora. Usados para deixar anotações no código.
  Sintaxe: `<!-- Isso é um comentário -->`

- **Anatomia das Tags**
  Uma tag possue uma abertura <tag>, conteúdo e fechamento </tag>.
  Exemplo: `<p>Olá mundo</p>`

- **Espaços e quebras de linha**
  O HTML ignora múltiplos espaços em branco.
  Para quebra de linha, usa-se a tag `<br>`

- **Fluxo HTML**
  A ordem em que o HTML é interpretado e exibido. Os elementos seguem uma hierarquia, do topo para o fim da página.

- **Alinhamento de Tags**
  Tags podem estar aninhadas (uma dentro da outra), respeitando a hierarquia do conteúdo.

- **Caracteres reservados**
  Alguns símbolos têm funções especiais no HTML, como <, >, &, etc. Para exibi-los, usamos entidades:
  Exemplo: `&lt;` para <, `&gt;` para >

---

### Atributos

- **O que são atributos?**
  Informações adicionais fornecidas às tags. São sempre definidos dentro da tag de abertura.
  Exemplo: `<a href="https://examplo.com">Link</a>`

- **Atributos booleanos**
  Atributos que não precisam de valor explícito. Ex: `disabled`, `checked`.

- **Atributos globais**
  Podem ser usados em qualquer elemento HTML. Ex: `id`, `class`, `style`, `data-*`.

- **Id**
  Identificador único para um elemento.
  Exemplo: `<div id="topo"></div>`

- **Class**
  Permite aplicar estilos a vários elementos.
  Exemplo: `<div class="card"></div>`

- **Data**
  Permite armazenar dados personalizados com o prefixo data-.
  Ex: `<div data-user="abimael"></div>`

- **Style**
  Define estilos inline diretamente no HTML.
  Evite o uso excessivo. Ex: `<p style="color:red;">Texto</p>`

---

### Elementos de conteúdo

- **Semântica**
  Usar tags que representam o significado do conteúdo. Ex: `<header>`, `<nav>`, `<footer>`

- **Títulos e Parágrafos**
  Tags de título: `<h1>` até `<h6>`.
  Parágrafo: `<p>`

- **Formatação Básica de Textos**
  Negrito: `<strong>` ou `<b>`
  Itálico: `<em>` ou `<i>`
  Sublinhado: `<u>`

- **Listas**
  Ordenadas: `<ol>`, com `<li>`
  Não ordenadas: `<ul>`, com `<li>`

- **Representação de Código**
  Tag `<code>` representa código-fonte.
  Pode ser usada junto com `<pre>` para manter a formatação.

- **Hiperlink**
  Tag `<a href="url">` cria um link. Pode abrir em nova aba com `target="_blank"`

- **Imagens**
  Tag `<img src="caminho" alt="descrição" />`.
  Atributo `alt` é essencial para acessibilidade.

---

### Elementos estruturais

- **Anatomia de um documento HTML**

  ```html
  <!DOCTYPE html>
  <html lang="pt-BR">
    <head>
      <meta charset="UTF-8" />
      <title>Título</title>
    </head>
    <body>
      <!-- Conteúdo -->
    </body>
  </html>
  ```

- **Desenhando uma página web**
  Definir seções bem organizadas com semântica adequada, facilitando a leitura e manutenção.

- **Tags Semânticas**
  `<header>`: Cabeçalho da página ou seção
  `<main>`: Conteúdo principal
  `<aside>`: Conteúdo complementar
  `<footer>`: Rodapé da página
  `<nav>`: Navegação
  `<section>`: Seção do conteúdo
  `<article>`: Conteúdo independente (ex: post)

- **Tags Genéricas**
  `<div>`: Agrupamento genérico (sem significado)
  `<span>`: Para estilizar partes de textos inline

---

### Caminhos absolutos e relativos

- **Caminho absoluto local:**
  ```html
  <img src="C:/Users/abimael/projetos/imagens/foto.jpg" alt="Foto local" />
  ```
- **Relativo à mesma pasta:**
  ```html
  <img src="imagem.jpg" alt="Imagem" />
  ```
- **Relativo em subpastas:**
  ```html
  <img src="img/foto.jpg" alt="Foto" />
  ```
- **Relativo à pasta anterior:**
  ```html
  <img src="../foto.jpg" alt="Foto de outra pasta" />
  ```
- **Relativo ao servidor (root):**
  ```html
  <img src="/imagens/banner.jpg" alt="Banner do site" />
  ```

---

## CSS

CSS (Cascading Style Sheets) é a linguagem usada para estilizar elementos escritos em HTML. Ele controla a aparência visual de uma página web, como cores, tamanhos, espaçamentos, fontes e layout.

---

### Conhecendo o CSS

- **O que é o CSS**  
  CSS (Cascading Style Sheets) define o estilo de elementos HTML.

- **Comentários**  
  Feitos assim: `/* comentário */`

- **Anatomia de uma regra CSS**

  ```css
  seletor {
    propriedade: valor;
  }
  ```

- **Cascading**
  Quando há conflito de estilos, o navegador decide qual aplicar com base na ordem, herança e especificidade.

- **Especificidade e mais específico**
  Entender o "peso" dos seletores (inline > id > class > tag).

- **Valores e Unidades de medida**
  `px`, `em`, `rem`, `%`, `vh`, `vw`, etc.

- **Seletores**
  Simples (.classe, #id, elemento) e avançados ([attr], :hover, ::after, etc.).

- **Combinators**
  Seletores simples e combinadores (`>`, `+`, `~`)
  Descendente: `div p`
  Filho direto: `div > p`
  Irmão adjacente: `div + p`
  Irmão geral: `div ~ p`

- **Formas de adicionar CSS**
  Inline (`style="..."`)
  Interno (dentro de `<style>`)
  Externo (`link href="estilo.css"`)

---

### Box Model

Todo elemento HTML é uma caixa (box):

- **Box Model**
  Inclui: `content + padding + border + margin`

- **Display**
  Tipos de display: `block`, `inline`, `inline-block`, `none`, `flex`, `grid`

- **Dimensões**
  `width`, `height`

- **Espaçamento e bordas**
  `margin`, `padding`, `border`

- **Box-sizing**
  `content-box` ou `border-box`

---

### Fontes e Textos

- `font-family`
- `font-size`
- `font-style`, `font-weight`
- `color`, `text-align`, `line-height`, `text-transform`, `text-decoration`
- `letter-spacing`, `word-spacing`,
- `font` (shorthand)
- Uso de Web Fonts (ex: Google Fonts)

---

### Cores e Fundos

- **Tipos de cores**
  - Nomeadas: `blue`, `red`
  - RGB: `rgb(255, 0, 0)`
  - HSL: `hsl(0, 100%, 50%)`
- Fundos:
  - `background-color`
  - `background-image`
  - `background-repeat`
  - `background-position`
  - `background-size`
  - `background` (shorthand)

---
