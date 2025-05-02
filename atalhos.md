## Atalhos HTML no VS Code

Os atalhos no VS Code para HTML podem acelerar muito o seu fluxo de trabalho, permitindo que você escreva código de forma mais rápida e eficiente. Aqui estão alguns dos atalhos mais úteis e como aproveitá-los:


* **Estrutura básica de um documento HTML:** Digite `!` e pressione `Tab` ou `Enter`. Isso irá expandir para a estrutura básica do HTML:

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>

    </body>
    </html>
    ```

    Você pode até mesmo especificar o idioma, por exemplo, `!pt-BR` seguido de `Tab` para ter `<html lang="pt-BR">`.

* **Criação de elementos com tags:** Basta digitar o nome da tag e pressionar `Tab` ou `Enter`.
    * `div` + `Tab` → `<div></div>`
    * `p` + `Tab` → `<p></p>`
    * `span` + `Tab` → `<span></span>`

* **Adicionando classes e IDs:** Use a sintaxe do CSS para especificar classes (`.`) e IDs (`#`).
    * `.container` + `Tab` → `<div class="container"></div>`
    * `p#descricao` + `Tab` → `<p id="descricao"></p>`
    * `ul.lista-itens#principal` + `Tab` → `<ul class="lista-itens" id="principal"></ul>`

* **Criando múltiplos elementos:** Use o operador de multiplicação (`*`).
    * `li*5` + `Tab` → Cria 5 elementos `<li>` vazios.

        ```html
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        ```

    * `div.item*3` + `Tab` → Cria 3 `div`s com a classe `item`.

        ```html
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        ```

* **Criando elementos filhos:** Use o operador de filho (`>`).
    * `nav>ul>li*3>a` + `Tab` → Cria uma estrutura de navegação com uma lista não ordenada contendo 3 itens de lista, cada um com um link (`<a>`).

        ```html
        <nav>
            <ul>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
            </ul>
        </nav>
        ```

* **Criando elementos irmãos:** Use o operador de irmão (`+`).
    * `h2+p+ul>li*2` + `Tab` → Cria um `h2`, seguido por um `p`, seguido por uma `ul` com dois `li`s.

        ```html
        <h2></h2>
        <p></p>
        <ul>
            <li></li>
            <li></li>
        </ul>
        ```

* **Adicionando texto aos elementos:** Use chaves `{}`.
    * `h1{Meu Título}` + `Tab` → `<h1>Meu Título</h1>`
    * `li*3{Item $}` + `Tab` → Cria 3 `li`s com o texto "Item 1", "Item 2" e "Item 3" (o `$` é um contador).

        ```html
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        ```

* **Atributos personalizados:** Use colchetes `[]`.
    Você pode combinar os colchetes com outras funcionalidades, como classes (.), IDs (#) e operadores de filho (>) ou irmão (+).

    * `div.form-group>input[type="password" name="senha" id="senha-input"]`
    E pressione Tab ou Enter. O Emmet irá expandir para:

    ```HTML
    <div class="form-group">
        <input type="password" 
        name="senha" 
        id="senha-input">
    </div>
    ```

    Se você quiser criar vários links com URLs que seguem um padrão sequencial, o contador $ pode ser útil dentro do atributo href.

    Exemplo: Criar 3 links com hrefs como link1.html, link2.html, link3.html:

    Digite:



    `a[href="link$.html"]*3{Link $}`
     Pressione Tab. O resultado será:

    ```HTML

    <a href="link1.html">Link 1</a>
    <a href="link2.html">Link 2</a>
    <a href="link3.html">Link 3</a>
    ```