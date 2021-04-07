# INTRODUÇÃO

# — O que significa CSS?

- Cascading Style Sheet:
- Código para criar estilos no HTML;
- HTML é a estrutura, e o CSS é a estética;
- Não é uma linguagem de programação;
- É uma linguagem style sheet.

# Comentários

/\*\*/

# Anatomia

```CSS
element {
    property: valor;
    color: blue;
    font-size: 60px;
    background: gray;

}
```

- Selector: element
- Declaration: property
- Properties: valor
- Property Value

# Selectors

Conecta um elemento HTML com o CSS

## Tipos

- Global selector `*` <!-- Seleção global para alterar em todo o documento>
- Element/Type selector `h1, h2, p, div`
- ID Selector `#box, #container`
- Class Selector `.red, .m-4`
- Attribute selector, Pseudo-class, Pseudo-element e outros.

## Adicionando CSS

### inline

    — atributo `style`

## <style>

    — tag html que irá conter o CSS.

## <link>

    — arquivo css externo.

## @import

    — arquivo css externo.

## A Cascata (cascading)

Seu estilo é lido de cima para baixo, levando em consideração três fatores: 1. Origem do estilo;
inline >
tag style >
tag link.

    2. Especificidade;
        É um cálculo matemático onde cada seletor e origem de estilo, possuem valores a serem considerados.
        0) Universal selector, combinators e negation pseudo-class (:not())
        1) Element type selector e pseudo-elements (::before, ::after)
        10) Classes e attribute selector ([type="radio"]): `.class`
        100) ID selector `#id`
        1000) Inline.

    3. Importância.
    * cuidado, evite o uso;
    Não é considerada uma boa prática e quebra o fluxo natural da cascata.

## At-rules @

Está relacionado ao comportamento do css. Começa com o sinal `@` seguido do identificador e valor.

## Exemplos comuns

    - @import: incluir um CSS externo.
    - @media: regras condicionais para dispositivos.
    - @font-face: fontes externas.
    - @keyframes: animações.

## Shorthand

Junção de propriedades, resumida e legível.

```css
 {
  /*background properties*/
  background-color: #000;
  background-image: url(images/bg.gif);
  background-repeat: no-repeat;
  background-position: left top;

  /*background shorthands*/
  background: 000 url (images/bg.gif) no-repeat left top;

  /*font properties*/
  font-style: italic;
  font-weight: bold;
  font-size: 0.8em;
  line-height: 1.2;
  font-family: Arial, sans-serif;

  /*font shorthands*/
  font: italic, bold, 0.8em/1.2, Arial, sans-serif;
}
```

## Detalhes

Valor não especificado irá assumir o valor padrão. Geralmente, a ordem descrita não importa, mas, se houver muitas propriedades com valores semelhantes, podemos encontrar problemas.

## Funções

Nome seguido de abre e fecha parentesis. Recebe argumentos.

```css
@import url ("https://urlaqui.com/style.css");

 {
  color: rgb (255, 0, 100);
  width: calc(100%-10%);
}
```

## Vendor Prefixes

— Consulta:
[http://ireade.github.io/which-vendor-prefix/]
[https://caniuse.com/]
