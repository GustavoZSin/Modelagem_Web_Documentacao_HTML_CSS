# Projeto de Aprofundamento sobre HTML e CSS

## Capítulo 1: Introdução ao CSS

- **Objetivo:** Apresentar o que é CSS, sua importância e como ele se integra ao HTML.
- **Conteúdo:**
  - **O que é CSS:** CSS (Cascading Style Sheets) é a linguagem usada para estilizar páginas HTML, permitindo o controle visual de layouts, cores, fontes e outros elementos de design.
  - **Integração com HTML:** O CSS pode ser integrado ao HTML de três formas:
    - **Inline:** No atributo `style` de uma tag HTML.
      ```html
      <h1 style="color: red;">Título em vermelho</h1>
      ```
    - **Embutido:** Usando a tag `<style>` no documento HTML.
      ```html
      <style>
        body {
          background-color: lightblue;
        }
        h1 {
          color: darkblue;
        }
      </style>
      ```
    - **Externo:** Usando um arquivo CSS externo.
      ```html
      <link rel="stylesheet" href="styles.css" />
      ```
  - [**Exemplo Completo:**](./Capitulos/capitulo1.html)

## Capítulo 2: Selectores e Especificidade

- **Objetivo:** Explorar a lógica dos selectores e a hierarquia de estilos.
- **Conteúdo:**
  - **Selectores Básicos:** Como selecionar elementos HTML (por tag, id, classe) e aplicar estilos específicos.
    ```css
    h1 {
      color: blue;
    }
    .classe {
      font-size: 16px;
    }
    #id {
      background-color: yellow;
    }
    ```
  - **Selectores de Atributo:** Usar atributos de elementos HTML como critério de seleção.
    ```css
    input[type="text"] {
      border: 1px solid black;
    }
    a[href^="https"] {
      color: green;
    }
    ```
  - **Selectores de Descendentes:** Selecionar elementos baseados na hierarquia HTML.
    ```css
    div p {
      color: darkgray;
    } /* Seleciona todos os <p> dentro de <div> */
    div > p {
      font-weight: bold;
    } /* Seleciona <p> que são filhos diretos de <div> */
    ```
  - **Especificidade:** IDs têm maior prioridade que classes, e estas têm maior prioridade que tags. Quando estilos entram em conflito, o CSS usa um sistema de pontos para decidir qual regra aplicar.
    ```css
    #titulo {
      color: red;
    } /* prevalece sobre h1 */
    h1 {
      color: blue;
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo2.html)

## Capítulo 3: Cores e Unidades

- **Objetivo:** Aplicar cores e diferentes unidades de medida no CSS.
- **Conteúdo:**
  - **Cores no CSS:** Você pode usar diferentes formas de declarar cores:
    - Nomes de cores (ex.: `red`, `blue`).
    - Hexadecimal (`#ff0000`).
    - RGB (`rgb(255, 0, 0)`).
    - HSL (`hsl(0, 100%, 50%)`).
    ```css
    p {
      color: #ff0000;
    } /* Hexadecimal */
    p {
      color: rgb(255, 0, 0);
    } /* RGB */
    ```
  - **Unidades de Medida:** Medidas absolutas (px) vs. medidas relativas (em, rem, %).
    ```css
    .container {
      width: 50%;
    }
    .texto {
      font-size: 2rem;
    }
    ```
  - **Unidades Relativas para Layouts Flexíveis:**
    ```css
    .box {
      width: 80vw; /* 80% da largura da janela */
      height: 50vh; /* 50% da altura da janela */
    }
    ```
  - **Cores com Opacidade:** Usar `rgba` para definir transparência.
    ```css
    .box {
      background-color: rgba(0, 0, 255, 0.5); /* Azul com 50% de opacidade */
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo3.html)

## Capítulo 4: Tipografia e Fontes Customizadas

- **Objetivo:** Explorar como estilizar texto e incluir fontes personalizadas.
- **Conteúdo:**

  - **Fontes:** Definir famílias de fontes (serif, sans-serif), tamanho e peso das fontes.
    ```css
    body {
      font-family: "Arial", sans-serif;
    }
    h1 {
      font-size: 2em;
      font-weight: bold;
    }
    ```
  - **Outros Estilos Tipográficos:** Manipular espaçamento entre linhas (line-height), entre letras (letter-spacing), e o alinhamento do texto.
    ```css
    p {
      line-height: 1.5;
      letter-spacing: 2px;
      text-align: justify;
    }
    ```
  - **Fontes Customizadas com @font-face:** Para incluir uma fonte customizada em um projeto.

    ```css
    @font-face {
      font-family: "MinhaFonte";
      src: url("minha-fonte.woff2") format("woff2"), url("minha-fonte.woff")
          format("woff");
    }

    h1 {
      font-family: "MinhaFonte", sans-serif;
    }
    ```

  - **Exemplo com Google Fonts:**

    ```css
    @import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

    body {
      font-family: "Roboto", sans-serif;
    }
    ```

  - [**Exemplo Completo:**](./Capitulos/capitulo4.html)

## Capítulo 5: Box Model e Layout

- **Objetivo:** Apresentar o Box Model e como ele influencia o layout de uma página.
- **Conteúdo:**
  - **Box Model:** O Box Model define como o espaço de um elemento é calculado. Ele inclui:
    - **Content:** O conteúdo real.
    - **Padding:** Espaço interno entre o conteúdo e a borda.
    - **Border:** A borda ao redor do elemento.
    - **Margin:** O espaço externo entre o elemento e outros elementos.
    ```css
    .box {
      width: 200px;
      padding: 10px;
      border: 5px solid black;
      margin: 20px;
    }
    ```
  - **Box Sizing:** Controlar o tamanho total do elemento incluindo bordas e padding.
    ```css
    .box {
      box-sizing: border-box; /* Inclui padding e borda no cálculo do tamanho */
    }
    ```
  - **Exemplo com Overflows:**
    ```css
    .overflow-box {
      width: 150px;
      height: 150px;
      border: 2px solid red;
      overflow: scroll; /* Mostra barra de rolagem se o conteúdo exceder */
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo5.html)

## Capítulo 6: Flexbox

- **Objetivo:** Utilizar o Flexbox para criar layouts flexíveis e responsivos.
- **Conteúdo:**
  - **Flexbox:** O Flexbox facilita a criação de layouts flexíveis. Propriedades principais incluem:
    ```css
    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    ```
  - **Flexbox com direção de coluna:**
    ```css
    .vertical {
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      height: 400px;
    }
    ```
  - **Flex-wrap:** Forçar itens a quebrarem linha ao excederem o espaço.
    ```css
    .wrap {
      display: flex;
      flex-wrap: wrap;
    }
    .item {
      width: 150px;
      height: 150px;
      margin: 10px;
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo6.html)

## Capítulo 7: Grid Layout

- **Objetivo:** Apresentar o CSS Grid e suas capacidades para criação de layouts complexos.
- **Conteúdo:**
  - **Grid Layout:** Permite criar layouts de múltiplas colunas e linhas de forma fácil.
    ```css
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
    }
    ```
  - **Posicionamento de Itens no Grid:** Usar `grid-column` e `grid-row` para posicionar elementos.
    ```css
    .item1 {
      grid-column: 1 / 2;
      grid-row: 1 / 2;
    }
    .item2 {
      grid-column: 2 / 3;
      grid-row: 1 / 3;
    }
    ```
  - **Exemplo de Grid Responsivo:**
    ```css
    @media (max-width: 768px) {
      .container {
        grid-template-columns: 1fr;
      }
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo7.html)

## Capítulo 8: Estilização Avançada e Animações

- **Objetivo:** Explorar técnicas avançadas de estilização e introduzir animações em CSS.
- **Conteúdo:**
  - **Pseudo-classes e pseudo-elementos:** Manipular estados de elementos como `:hover`, `:before`, `:after`.
    ```css
    a:hover {
      color: red;
    }
    p::before {
      content: "Prefixo: ";
      color: gray;
    }
    ```
  - **Animações:** Criar transições e animações com `transition` e `keyframes`.
    ```css
    .box {
      transition: background-color 0.5s ease;
    }
    .box:hover {
      background-color: yellow;
    }
    @keyframes slideIn {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(0);
      }
    }
    .animado {
      animation: slideIn 1s ease-out;
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo8.html)

## Capítulo 9: Responsividade e Media Queries

- **Objetivo:** Criar layouts responsivos que se adaptam a diferentes dispositivos.
- **Conteúdo:**
  - **Media Queries:** Aplicar estilos diferentes com base no tamanho da tela.
    ```css
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
      }
    }
    ```
  - [**Exemplo Completo:**](./Capitulos/capitulo9.html)

## Capítulo 10: Boas Práticas e Otimização

- **Objetivo:** Consolidar os conceitos aprendidos e introduzir boas práticas e técnicas de otimização.
- **Conteúdo:**
  - **Boas práticas:** Manter o CSS organizado, evitar duplicação de código e utilizar nomes de classes claros.
    ```css
    /* Evite repetição de código */
    .button {
      padding: 10px 20px;
      border-radius: 5px;
    }
    .button-primary {
      background-color: blue;
      color: white;
    }
    .button-secondary {
      background-color: gray;
      color: black;
    }
    ```
  - **Otimização:** Minimizar o CSS, reduzir o uso de seletores complexos e evitar carregar arquivos CSS desnecessários para melhorar a performance.
    - Exemplo de minificação:
      ```css
      .container {
        display: flex;
        justify-content: space-between;
      }
      .item {
        width: 100px;
      }
      ```
  - [**Exemplo Completo:**](./Capitulos/capitulo10.html)