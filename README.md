# Projeto de aprofundamento sobre CSS

## Capítulo 1: Introdução ao CSS

- **Objetivo:** Apresentar o que é CSS, sua importância e como ele se integra ao HTML.
- **Conteúdo:**
  - **O que é CSS:** CSS (Cascading Style Sheets) é a linguagem usada para estilizar páginas HTML, permitindo o controle visual de layouts, cores, fontes e outros elementos de design.
  - **Integração com HTML:** O CSS pode ser integrado ao HTML de três formas: inline, embutido e externo (recomendado o uso de arquivos externos para melhor organização).
  - **Exemplo:**
    ```html
    <style>
      body {
        background-color: lightblue;
      }
    </style>
    ```

## Capítulo 2: Selectores e Especificidade

- **Objetivo:** Explorar a lógica dos selectores e a hierarquia de estilos.
- **Conteúdo:**
  - **Selectores Básicos:** Como selecionar elementos HTML (por tag, id, classe) e aplicar estilos específicos.
    ```css
    h1 { color: blue; }
    .classe { font-size: 16px; }
    #id { background-color: yellow; }
    ```
  - **Especificidade:** Regras sobre quais estilos prevalecem quando há múltiplos aplicáveis ao mesmo elemento. IDs têm maior prioridade que classes e estas têm maior prioridade que tags.
  - **Exemplo:**
    ```css
    #titulo { color: red; } /* prevalece sobre h1 */
    h1 { color: blue; }
    ```

## Capítulo 3: Cores e Unidades

- **Objetivo:** Aplicar cores e diferentes unidades de medida no CSS.
- **Conteúdo:**
  - **Cores no CSS:** Diferentes formas de declarar cores (nome, hexadecimal, RGB, HSL).
    ```css
    p { color: #ff0000; } /* Hexadecimal */
    p { color: rgb(255, 0, 0); } /* RGB */
    ```
  - **Unidades de medida:** Absolutas (px) vs. relativas (em, rem, %, vw, vh).
    ```css
    .container { width: 50%; }
    .texto { font-size: 2rem; }
    ```

## Capítulo 4: Tipografia

- **Objetivo:** Explorar como estilizar texto e escolher fontes adequadas.
- **Conteúdo:**
  - **Fontes:** Definir famílias de fontes (serif, sans-serif), tamanho e peso das fontes.
    ```css
    body { font-family: 'Arial', sans-serif; }
    h1 { font-size: 2em; font-weight: bold; }
    ```
  - **Outros Estilos Tipográficos:** Espaçamento entre linhas (line-height), entre letras (letter-spacing), alinhamento de texto.
    ```css
    p { line-height: 1.5; letter-spacing: 2px; text-align: justify; }
    ```

## Capítulo 5: Box Model e Layout

- **Objetivo:** Apresentar o Box Model e como ele influencia o layout de uma página.
- **Conteúdo:**
  - **Box Model:** Conceito de conteúdo, padding, border e margin. Como cada um influencia o espaço e o tamanho dos elementos.
    ```css
    .box {
      width: 200px;
      padding: 10px;
      border: 5px solid black;
      margin: 20px;
    }
    ```
  - **Exemplo prático:** Criar uma estrutura básica com box model para visualizar os efeitos de padding e margin.

## Capítulo 6: Flexbox

- **Objetivo:** Utilizar o Flexbox para criar layouts flexíveis e responsivos.
- **Conteúdo:**
  - **Propriedades principais:** `display: flex;`, `justify-content;`, `align-items;`, `flex-direction;`.
    ```css
    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    ```
  - **Exemplo:** Organizar elementos em um layout flexível que se adapta a diferentes tamanhos de tela.

## Capítulo 7: Grid Layout

- **Objetivo:** Apresentar o CSS Grid e suas capacidades para criação de layouts complexos.
- **Conteúdo:**
  - **Definir um Grid:** Utilizar `grid-template-columns` e `grid-template-rows` para criar layouts de várias colunas e linhas.
    ```css
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
    }
    ```
  - **Exemplo:** Criar um layout de página com cabeçalho, corpo e rodapé usando CSS Grid.

## Capítulo 8: Estilização Avançada e Animações

- **Objetivo:** Explorar técnicas avançadas de estilização e introduzir animações em CSS.
- **Conteúdo:**
  - **Pseudo-classes e pseudo-elementos:** Manipular estados de elementos como `:hover`, `:before`, `:after`.
    ```css
    a:hover { color: red; }
    ```
  - **Animações:** Criar transições e animações com `transition`, `keyframes`.
    ```css
    .box {
      transition: background-color 0.5s ease;
    }
    .box:hover {
      background-color: yellow;
    }
    ```

## Capítulo 9: Responsividade e Media Queries

- **Objetivo:** Criar layouts responsivos que se adaptam a diferentes dispositivos.
- **Conteúdo:**
  - **Media Queries:** Aplicar estilos diferentes com base no tamanho da tela.
    ```css
    @media (max-width: 768px) {
      .container { flex-direction: column; }
    }
    ```
  - **Exemplo:** Ajustar um layout para que fique legível e organizado tanto em dispositivos móveis quanto em desktops.

## Capítulo 10: Boas Práticas e Otimização

- **Objetivo:** Consolidar os conceitos aprendidos e introduzir boas práticas e técnicas de otimização.
- **Conteúdo:**
  - **Boas práticas:** Manter o CSS organizado, evitar duplicação de código e utilizar nomes de classes claros.
  - **Otimização:** Minimizar o CSS, reduzir o uso de seletores complexos e evitar carregar arquivos CSS desnecessários para melhorar a performance.
  - **Exemplo:** Uso de ferramentas de minificação como o `CSSNano` para reduzir o tamanho do arquivo final de CSS.
