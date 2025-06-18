# Avançando no HTML e CSS

Este documento contém conteúdos mais avançados sobre HTML e CSS, com foco em técnicas modernas de layout como Flexbox, Grid e posicionamento de elementos na página.

---

## Layout e Evolução do CSS

### Normal Flow

- O fluxo normal do HTML/CSS, onde elementos `block` ocupam toda a largura disponível e elementos `inline` apenas o necessário para seu conteúdo.

### Tabelas (Table Layout)

- Layout baseado em tabelas era comum antes do CSS moderno.
- `display: table`, `table`, `tr`, `td`, entre outras, eram usados para estruturar páginas.
- Hoje é desaconselhado para layout, mas útil para dados tabulares.

### Tableless (Layout sem Tabela)

- Abordagem moderna que evita o uso de tabelas para layout.
- Utiliza `float: left` e `clear: both` para dispor elementos.
- Ainda usado em alguns contextos, mas Flexbox e Grid são mais poderosos.

---

## Flexbox

Sistema de layout unidimensional para alinhar e distribuir elementos em containers.

### Conceitos

- Flex container: elemento com `display: flex`
- Flex items: elementos filhos do container

### Eixos

- **Main Axis (eixo principal)**: depende de `flex-direction`
- **Cross Axis (eixo cruzado)**: perpendicular ao main axis

### Direção

- `flex-direction`: row, row-reverse, column, column-reverse

### Alinhamento e Espaços

- `justify-content`: alinha no eixo principal
- `align-items`: alinha no eixo cruzado
- `gap`: espaçamento entre os itens
- `margin: auto`: centraliza elementos

### Quebra de Linha

- `flex-wrap`: wrap, nowrap, wrap-reverse
- `align-content`: alinha múltiplas linhas

### Tamanhos Flexíveis

- `flex-basis`: tamanho inicial do item
- `flex-grow`: quanto o item cresce
- `flex-shrink`: quanto o item encolhe
- `flex`: shorthand para grow, shrink e basis

### Ordem

- `order`: muda a ordem visual (atenção à acessibilidade)

### Container

- `display: flex`
- `flex-flow`: shorthand para direction + wrap
- `row-gap`, `column-gap`, `justify-content`, `align-items`, `align-content`

### Children (Itens)

- `flex`, `flex-grow`, `flex-shrink`, `flex-basis`, `align-self`

---

### Position

Controla o posicionamento dos elementos na página.

- `static`: padrão
- `relative`: relativo à posição original
- `absolute`: sai do fluxo, relativo ao ancestral posicionado
- `fixed`: fixo na tela (viewport)
- `sticky`: alterna entre relativo e fixo, conforme o scroll
- Propriedades: `top`, `bottom`, `left`, `right`, `inset`, `z-index`

---

### Variáveis no CSS

Permitem reutilização de valores.

- **Criação:** `--cor-principal: #ff0000;`
- **Uso:** `var(--cor-principal)`
- **Escopo:** definidas no `:root` (global) ou em elementos específicos (local)

---

### Pseudo-classes

- Interações e estados dos elementos
- Exemplos:
  - `:hover`
  - `:not()`, `:has()`
  - `:root`, `:nth-child(n)`

---

### Pseudo-elements

- Criam partes fictícias do elemento
- Exemplos:
  - `::before`, `::after`
  - `::first-letter`

---

## CSS Grid

**CSS Grid** é um sistema de layout bidimensional poderoso para organizar elementos na tela.

### Estrutura básica

Todo Grid é composto por dois principais elementos:

- `Container` (elemento pai)
- `Itens` (elementos filhos)

---

#### Propriedades do Container (pai)

- `display: grid`  
  Ativa o comportamento de grid no elemento pai.

- `grid-template` (shorthand)

  - `grid-template-columns`  
    Define as colunas do grid  
    Ex: `1fr 1fr 1fr` ou `repeat(3, 1fr)`
  - `grid-template-rows`  
    Define as linhas do grid  
    Ex: `200px 1fr 2fr`
  - `grid-template-areas`  
    Permite nomear áreas para facilitar o posicionamento

- `gap`  
  Espaçamento entre linhas e colunas
  - `row-gap`
  - `column-gap`

---

#### Propriedades dos Itens (filhos)

- `grid-column` (shorthand)

  - `grid-column-start`
  - `grid-column-end`

- `grid-row` (shorthand)

  - `grid-row-start`
  - `grid-row-end`

- `grid-area`  
  Usada para nomear ou posicionar o item dentro de uma área nomeada.

---

### Alinhamento

Existem 9 propriedades importantes para alinhamento. Elas se dividem em 3 grupos e podem ser aplicadas no container ou nos itens:

#### No Container (pai)

- `align-content` – alinha o **conteúdo** no eixo vertical
- `justify-content` – alinha o **conteúdo** no eixo horizontal
- `place-content` – shorthand: `align-content + justify-content`

- `align-items` – alinha os **itens** no eixo vertical
- `justify-items` – alinha os **itens** no eixo horizontal
- `place-items` – shorthand: `align-items + justify-items`

#### Nos Itens (filhos)

- `align-self` – alinha o **próprio item** verticalmente
- `justify-self` – alinha o **próprio item** horizontalmente
- `place-self` – shorthand: `align-self + justify-self`

---

### Propriedades automáticas

Essas propriedades são usadas para gerar linhas/colunas automaticamente com base no conteúdo:

- `grid-auto-flow`
  - Define a direção automática de preenchimento (`row`, `column`)
- `grid-auto-rows`
  - Altura padrão de linhas criadas automaticamente
- `grid-auto-columns`
  - Largura padrão de colunas criadas automaticamente

---

## Grid ou Flex

| Critério        | Flexbox                              | Grid                               |
| --------------- | ------------------------------------ | ---------------------------------- |
| Direção         | Unidimensional (linha **ou** coluna) | Bidimensional (linha **e** coluna) |
| Layout complexo | Difícil de manter                    | Mais organizado                    |
| Controle visual | Menor                                | Maior                              |
| Alinhamento     | Ótimo em uma direção                 | Ótimo em ambas as direções         |

**Regra geral**:

- Use **Flexbox** para layouts lineares simples (menus, cards, botões).
- Use **Grid** para **disposição mais complexa** de elementos em colunas e linhas.

---
