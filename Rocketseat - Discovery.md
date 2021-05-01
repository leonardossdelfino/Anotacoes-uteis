### Rocketseat 

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

