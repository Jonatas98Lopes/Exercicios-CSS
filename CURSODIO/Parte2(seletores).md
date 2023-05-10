# Fundamentos do CSS


## Seletores

Nós temos seletores no CSS. Um seletor define quais elementos receberão a estilização CSS. Vamos ve-los agora!

### Seletores de Tag

O seletor de tag nada mais é do que usar o nome da tag para selecionar o elemento que quer estilizar. Ele vai estilizar todos os elementos HTML que tem aquela tag.

```
h1 {
    background-color: red;
    color: white;
}
```
*** 

### Seletores de ID

O seletor por ID serve para identificar um elemento único na sua página HTML. Imagine que você tivesse 10 tags **p** no seu HTML e quisesse formatar apenas a primeira. 

```
<body>
    <p>Parágrafo 1</p>
    <p>Parágrafo 2</p>
    <p>Parágrafo 3</p>
    <p>Parágrafo 4</p>
    <p>Parágrafo 5</p>
    <p>Parágrafo 6</p>
    <p>Parágrafo 7</p>
    <p>Parágrafo 8</p>
    <p>Parágrafo 9</p>
    <p>Parágrafo 10</p>
</body>
```
Neste caso, você não poderia usar o seletor de tag, pois ele formataria todos.

Para isso, nós temos o **seletor de ID**. Como usá-lo?
* Primeiro você precisa adicionar o atributo **id** na tag em que quer estilizar;
```
<body>
    <p id="">Parágrafo 1</p>
    <p>Parágrafo 2</p>
    <p>Parágrafo 3</p>
    <p>Parágrafo 4</p>
    <p>Parágrafo 5</p>
    <p>Parágrafo 6</p>
    <p>Parágrafo 7</p>
    <p>Parágrafo 8</p>
    <p>Parágrafo 9</p>
    <p>Parágrafo 10</p>
</body>
```
* Adicionar um valor(NÃO PODE CONTER ESPAÇOS) ao atributo; 
```
<body>  
    <p id="meu-primeiro-elemento">Parágrafo 1</p>
    <p>Parágrafo 2</p>
    <p>Parágrafo 3</p>
    <p>Parágrafo 4</p>
    <p>Parágrafo 5</p>
    <p>Parágrafo 6</p>
    <p>Parágrafo 7</p>
    <p>Parágrafo 8</p>
    <p>Parágrafo 9</p>
    <p>Parágrafo 10</p>
</body>
```
* E usar o seletor de ID do CSS.

```
<style>
    #meu-primeiro-elemento {
        background-color: blue; 
        color: white; 
    }
</style>
```
*** 

### Seletores de Classes

O seletor de Classes é parecido com o de ID. A diferença é a utilidade dos atributos **id** e **class** no HTML. No HTML, você usa id como identificador único de elementos e você não pode repetir o mesmo ID em outro elemento. Já a class, é utilizada para juntar vários elementos numa mesma classe para que possamos estilizar. 

Considere o seguinte exemplo: Nós temos 5 parágrafos do texto 1 e mais 5 do texto 2. Nós queremos formatar todos os parágrafos, porém, queremos estilizar os parágrafos do texto 1 de uma forma, e os do texto 2 de outra forma. Como fazer isso uma vez que se o usarmos o seletor de tag, todos os parágrafos serão estilizados de forma igual?
```
<body>
    <div class="texto1">  
        <p>Parágrafo 1</p>
        <p>Parágrafo 2</p>
        <p>Parágrafo 3</p>
        <p>Parágrafo 4</p>
        <p>Parágrafo 5</p>
    </div>
    <div class="texto2">
        <p>Parágrafo 1</p>
        <p>Parágrafo 2</p>
        <p>Parágrafo 3</p>
        <p>Parágrafo 4</p>
        <p>Parágrafo 5</p>
    </div>
</body>

```

Neste caso, o **seletor de classes** será fundamental para nós. Vamos usá-lo agora dentro de uma tag style.

```
<style>
    .texto1 {
        color: blue;
    }
    .texto2 {
        color: red;
    }
</style>
```
IMPORTANTE: ASSIM COMO NOS VALORES DO ATRIBUTO ID, VOCÊ NÃO PODE DEIXAR ESPAÇOS DENTRO DE UM ATRIBUTO CLASS. SE FIZER ISSO, O CSS ENTENDERÁ  QUE TEMOS MAIS DE UMA CLASSE NO NOSSO HTML.

EXEMPLO:

```
<body>
     <div class="texto1 meu-primeiro-texto">  
        <p>Parágrafo 1</p>
        <p>Parágrafo 2</p>
        <p>Parágrafo 3</p>
        <p>Parágrafo 4</p>
        <p>Parágrafo 5</p>
    </div>
</body>
```
1ª classe: texto1

2ª classe: meu-primeiro-texto
*** 

### Seletores de Universais

Como o próprio nome diz, ele é universal, ou seja, a formatação que você aplicar nele, estilizará TODOS os elementos da sua página. Isso é muito útil quando queremos definir propriedades padrões para nossa página. Exemplo: Fontes, cores, fundos, etc...

Como usá-lo?
```
* {
    background-color: black;
    color: white;
}
```
Use apenas o asterisco, abrindo e fechando chaves. Tudo que você colocar entres as chaves será aplicado para toda a página.

*** 

### Seletores de Atributo

Às vezes, precisamos ser mais específicos e identificar um elemento por um atributo diferente de id ou classe. Considere o seguinte exemplo:

```
<body>
    <a title="Entre no Google." href="https://www.google.com">Google</a>
    <a title="Entre no YouTube." href="https://www.youtube.com">Youtube</a>
    <a title="Entre no Facebook." href="https://www.facebook.com">Facebook</a>
    <a href="https://www.instagram.com">Instagram</a>    
</body>
```
Veja que neste exemplo, temos 4 tags **a** para mandar os usuários para os sites determinados. Dentre elas, 3 tags tem o atributo **title**. E se quiséssemos adicionar uma cor amarela a todas as tags que têm este atributo?

```
<style>
    [title] {
        color: yellow;
    }
</style>
```
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *]* { *PROPRIEDADES*}
Neste caso, das 4 tags somente as 3 primeiras receberiam a estilização. Isto é válido para qualquer atributo diferente de **id** ou **class**. 
Agora e se quiséssemos ser mais específicos ainda. Por exemplo, queremos colocar a cor verde somente no atributo **title** com o valor **Entre no Google**. Como faríamos isso?

```
<style>
    [title="Entre no Google"] {
        color: green;
    }
</style>
```
Lembre-se que os valores passados aqui precisam ser exatamente iguais aos do HTML.
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Outra forma de identificar esse mesmo elemento é pegar um trecho do valor do atributo, no caso **Entre no Google**. E se eu não lembrasse todo esse texto completo. Como identificá-lo?

Neste caso, podemos usar o operador que busca um texto separado por espaços antes dele ou depois dele.

```
<style>
    [title~="Google"] {
        color: green;
    }
</style>
```
Neste caso, estamos considerando que só lembramos da palavra Google no valor do atributo.
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *~* + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Imagine o seguinte código HTML:

```
<body>
    <p title="paragrafo-importante">Parágrafo 1</p>
    <p title="paragrafo">Parágrafo 2</p>
</body>
```
Existe um operador que poderia encontrar ambos aqui. Vamos usá-lo agora.
```
<style>
    [title|="paragrafo"] {
         color: gray;
    }
</style>
```
Esse operador identifica valores de atributo com o texto exato passado dentro dele, no caso "**paragrafo**", **ou** valores de atributos que contenham a palavra e um hífen a frente dela, no caso "**paragrafo-**importante"
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *|* + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Podemos também encontrar elementos cujos os valores do atributo começam com alguma palavra específica. 

Considere o seguinte código HTML.
```
<body>
    <p title="crucial">Parágrafo 1</p>
    <p title="mais que crucial">Parágrafo 2</p>
</body>
```
Se quisermos encontrar apenas o segundo parágrafo, podemos utilizar o código abaixo:

```
<style>
    [title^="mais"] {
        color: red;
    }
</style>
```
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *^* + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Podemos também encontrar valores que terminam com determinada palavra.

Considere o seguinte código HTML.
```
<body>
    <p title="importante">Parágrafo 1</p>
    <p title="importante sim">Parágrafo 2</p>
</body>
```
Vamos achar o segundo parágrafo com esse operador.
```
<style>
    [title$="sim"] {
        color: blue;
    }
</style>
```
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *$* + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Por último, podemos procurar por ocorrências de fragmentos de texto num atributo.

Considere o exemplo:
```
<body>
    <a title="Entre no Google." href="https://www.google.com">Google</a>
</body>
```

Podemos identificá-lo da seguinte forma:

```
<style>
    [title*=" no"]{
        color: blue;
    }
</style>
```
Ele vai procurar essa ocorrência dentro do valor do atributo.
SÍNTAXE: *[* + *NOMEDOATRIBUTO* + *** + *=* + *"* + *VALORDOATRIBUTO* + *"* + *]* { *PROPRIEDADES*}

Agora fica muito mais simples selecionar elementos para estilização! :)