# Fundamentos do CSS


## Introdução ao CSS

### O que é CSS?

Conhecido como Cascading Style Sheets(CSS) ou Folha de Estilo em Cascata é um mecanismo para adicionar estilos a um documento web(HTML).

Foi criado para facilitar o desenvolvimento web.

CSS não é uma linguagem de programação, mas sim, uma linguagem de estilos.

***

### O que pode ser criado com CSS?

* Layouts e estilização de páginas web;
* Animações;
* Formas geométricas e desenhos;
* Filtros;
* Contadores;

***

### Formas de Declaração do CSS

No seu CSS nós temos duas nomenclaturas fundamentais:

* **propriedade**: É uma característica de um elemento HTML como, cores, largura e altura, por exemplo.

* **valor**: É o valor que é adicionado a essa propriedade.

Forma de declaração de propriedades no CSS: **propriedade** + **:** + **valor** + **;**

Exemplo: 

```
background-color: red;
color: white;
```

Ok, mas... Como eu declaro isso nas minhas páginas HTML?

Nós temos três formas de fazer:

**CSS inline**: Adicionamos o código CSS diretamente dentro da tag através do atributo **style**.

Exemplo:

```
<h1 style="background-color: black;">Exemplo 1</h1>
```

O problema dessa forma é que se eu tem um padrão de estilo para todas as tags **p**, por exemplo, eu teria que aplicar a formatação em cada uma delas.


**CSS interno**: Aqui, nós adicionamos a **tag style**, não atributo **style**. Essa tag é adicionada dentro do *head* da página HTML e dentro dela, inserimos todo o código CSS que queremos.

Exemplo:

```
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <style>
        h1 {
        background-color: black;
        color: red;
        }
        </style>
    </head>
</html>

```

É uma forma mais organizada de estilizar o HTML, mas não é a ideal. Lembre-se que o método inline sempre tem prioridade.

Porém a gente não consegue reaproveitar o código para outras páginas.


**CSS externo**: é criado um arquivo com extensão **.css** que carregará a estilização daquele HTML. Em cada página HTML que desejar usar essa estilização, você informa esse arquivo CSS através da tag **link**.

Exemplo do que fazer no HTML:

```
<link rel="stylesheet" href="./assets/css/style.css">
```

A tag **link** é utilizada para determinar uma relação entre o arquivo HTML atual e um arquivo externo.

O atributo **rel** define que tipo de relação existe entre esse arquivos. Agora, podemos reutilizar esse código em quantas páginas quiser.

***

### Depuração CSS

Como debugar o código CSS.

Neste caso, vamos utilizar a ferramenta **Dev Tools**, também conhecido como **Inspetor de Elementos**. Na aba styles, nós temos  o CSS aplicado. Note que as propriedades CSS que estiverem itálico ali, são propriedades que são adicionadas ao código HTML pelo navegador automaticamente. Você também pode notar, que algumas propriedades estão apagadas e outras, vermelho mais escuro. As apagadas são o navegador quem coloca e as escuras, você.

Podemos ver os designs responsivos e mudar os dispositivos que acessam o site também.
