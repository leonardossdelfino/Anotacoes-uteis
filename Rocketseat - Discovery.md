Rocketseat 

### Discovery - Guia Estelar



---------------

#### Links úteis

**DevDocs (https://devdocs.io/http/status)**

----------------------



#### HTPP

**Idempotente**: Quando a resposta é sempre igual, quando faço uma atualização ele me retorna sempre a mesma coisa.

<u>**Métodos**</u>

**OPTIONS**: Recebe informações sobre a requisição e o que ele fornece tipo GET, POST, PUT, etc. *(curl -X OPTIONS http://localhost:3000/posts -i)*

**GET:** Ele pega recursos, só recebe dados, é respondido com um BODY.
*(curl -v* [*http://localhost:3000/posts*](http://localhost:3000/posts)).

**HEAD:** Semelhante ao GET, porém sem resposta e sem solicitação, não usado em formulário HTML. 

**POST:** Publicar, cadastrar um recurso. Existe body na requisição e na resposta, Formulário HTML sim.

**PUT:** Atualiza ou cria um recurso. Serve mais para atualizar. BODY no pedido.

**PATH:** Modificação ou parcial de um recurso. Path atualiza algumas valores, PUT atualiza por completo. Na teoria.

**DELETE:**  Remove um recurso.

**-X:** É o método a ser executado, OPTIONS, GET, POST, HEAD, PUT ou DELETE.



**Habilitar execução de scripts no PowerShell:**

`set-executionpolicy remotesigned -Scope CurrentUser`



---------



#### Headers

Cabeçalhos, informações adicionais para pedidos e respostas (nome:valor)
Ex: *content-type:application/json*

- **General**
  - Cabeçalho geral, tanto para informações do pedido quanto da resposta.

- **Response Headers**
  - authority: google.com – method: GET – path: / 

- **Request Headers**
  - cache-control: public, max-age=259200 (tempo de vencimento)
  - content-control: br (linguagem)

 

#### **Status Code**

1. Informational responses (100–199)
2. Successful responses (200–299)
3. Redirects (300–399)
4. Client errors (400–499)
5. Server errors (500–599)



------



#### CSS

**Selectors**

Conecta um elemento HTML com o CSS

**Tipos**

- Global selector `*`
  - Quando usado ele aplica a propriedade para todos os elementos.
- Element/Type selector `h1, h2, p, div`
- Class Selector `.red, .m-4`
- Para usar um `id` no CSS usa `#`. Ex: `#container`
- Para usar uma `class` no CSS usa `.`. Ex: `.m-40` ("margem 40px")
- Attribute selector, Pseudo-class, Pseudo-element, e outros.



**Box model**

Tudo basicamente são caixas, o conteúdo é organizado em caixas alinhadas no nosso site.



### Adicionando o CSS no documento HTML

````html
<!-- Inline -->
<h1 style="color: red;">TEXTO</h1>
````

`````html
<!-- No HTML -->
<head>
    <style>
        h1 { color: "red" }
    </style>
</head>
`````

````html
<!-- Usando uma folha de estilo a parte -->
<link rel="stylesheet" href="style.css">

<!-- Criado um arquivo <u>style.css</u> colocado dentro da mesma pasta do HTML ou em outro diretório. -->
````



### Especificidade (força)

`* { }`: Seletor universal - Valor 0 - (:not())

`h1 {}, h2 {}, body {}, etc`: Element selector e pseudo-elements (::before, ::after)  - Valor 1

class: `HTML(<h1 class="title">Título</h1>)`  `style.css(.title{ color: red; })` - Valor 10

id: `HTML(<h1 id="title">Título</h1>)` `style.css(#title{ color: red; }` - Valor 100

inline: Valor 1000



**Agrupamentos**



HTML

````html
<h1 class="title" id="title">TEXTO</h1>
````

CSS

````css
h1.title#title { color: "red"; }
````

Especificando o mais ainda dentro do h1

````css
#title strong { color: "gray" }
````



**!important**

Sobreescreve todas as outras regras.
Geralmente usado quando estamos usando o css de outra pessoa, fora isso não usar.

````css
`h1 { color: "red" "important"; }`
````



## Exemplo

<img src="C:\Users\Leonardo\Documents\GitHub\Anotacoes-uteis\HTML-1619970727418.png" alt="HTML" style="zoom:33%;" />

<img src="C:\Users\Leonardo\Documents\GitHub\Anotacoes-uteis\CSS-1619970732648.png" style="zoom: 50%;" />



### Regras com @

**Exemplos comuns**

- **@import:** incluir um CSS externo 
  - @import "http://local.com/style.css"
- **@media:** regras condicionais para dispositivos
  - @media (min-width: 500px)
- **@font-face:** fontes externas
  - @fontface {}
- **@keyframes:** Animation
  - @keyframes nameofanimation {}

### Shorthand

````css
{
    /* background properties */
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;
    
    /* background shorthand */
    background: #000 url(images/bg.gif) no-repeat left top;
    
    /* font properties */
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    font-height: 1.2;
    font-family: Arial, sans-serif;
    
    /* font shorthand */
    font: italic bold .8em/1.2 Arial, sans-serif;
}
````

**Detalhes**

- não irá considerar propriedades anteriores
- valores não especificados irão assumir o valor padrão da font
- geralmente, a ordem descrita não importa, mas, se houver muitas propriedades com valores semelhantes poderemos encontrar problemas

**Propriedades que aceitam shorthand**

**https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties**



### Funções

**Funções**

- nome seguido de abre e fecha parentesis
- recebe argumentos, ficam dentro dos parentesis

**Exemplos**

`````css
@import url("http://urlaqui.com/style.css")

{
    color: rgb(255,0,100);
    width: calc(100% - 10px);
}
`````



### Vendor Prefixes - Compatibilidade com os browser

Permite que browsers adicione **features** a fim de colocar em uso novidades que vemos no CSS.

**Exemplo**

````css
p {
    -webkit-background-clip: text; /* Chrome, Safari, iOS e Android */
    -moz-background-clip: text; /* Mozilla (Firefox) */
    -ms-background-clip: text; /* Internet Explorer */
    -o-background-clip: text; /* Opera */
}
````



**Consultas**

http://ireade.github.io/witch-vendor-prefix/

http://caniuse.com



----------



# Javascript

**String**: Cadeia de cadeia de caracteres

````javascript
// Interpolação
console.log(`${1 + 1}`)
````

**Number**: Números

**Boolean**: True ou False

**Undefinide x Null**: 

- <u>undefinide</u>
  - Indefinido
- <u>null</u>
  - nulo
  - objeto que não possui nada dentro
  - diferente de indefinido

**Object**:

-  Objeto
- Propriedades / Atributos
- Funcionalidades / Métodos

````javascript
const obj = {
    propriedade: "valor"
}
````

**Array**: 

- Uma lista
- Agrupamento de dado

`````javascript
const lista = ["Leo", 31]
`````



## Scope

**Block statement**: Declaração de bloco

**Hoisting**: O **JS** eleva a variável **var** para o topo, pois ela é global, mesmo eu chamando ela antes de declarar ele vai encontrar.