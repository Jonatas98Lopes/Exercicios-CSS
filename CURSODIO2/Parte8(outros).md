# Apresentação à Estilização Básica com CSS

## Outras

Vamos ver alguns propriedades sem uma ordem específica aqui.

### Aplicando Transparência aos Elementos

Nesta aula, vamos ver a propriedade **opacity**. Essa propriedade funciona exatamente as propriedades da função RGBA, quando trata-se do valor de transparência. Essa propriedade pode receber valores 0 a 1, onde 0 seria um elemento totalmente transparente e 1, totalmente vísivel.

Exemplo 100% transparente.
```
opacity: 0;
```
Exemplo 50% transparente.
```
opacity: 0.5;
```
Exemplo 0% transparente.
```
opacity: 1;
```
***

### Propriedade Overflow

Agora, vamos ver a propriedade **overflow**. Essa propriedade é realmente importante quando nosso texto ultrapassa os limites do container. Com ela, conseguimos definir o que acontecerá, caso isso aconteça.

Essa propriedade aceita alguns valores:

* **visible(padrão)**: Esse é o valor padrão. Quando fazemos isso, o conteúdo será exibido mesmo passando os limites do elemento.
```
overflow: visible;
```
* **hidden**: Esse valor esconde o conteúdo que ultrapassar o container do elemento. Será **impossível** acessar o que ultrapassou esse limite.
```
overflow: hidden;
```
* **scroll**: Esse valor esconde o conteúdo que ultrapassa o container, mas criará uma barra de rolagem para esse conteúdo. Criará uma barra de rolagem mesmo se o conteúdo for menor que o container.
```
overflow: scroll;
```
* **auto**: Como próprio nome diz, ele é automático, ou seja, se o conteúdo for menor que o container, tudo será exibido sem uma barra de rolagem como no valor **visible**. Todavia, caso, ultrapasse, ele cria uma barra de rolagem como **scroll**.
```
overflow: auto;
```

Lembre-se que para usar essa propriedade você precisa definir a altura do elemento e o elemento precisa ser **display: block;**

Existem duas variações dessa propriedade: o **overflow-x**, que configura apenas a parte horizontal, e o **overflow-y** apenas para a parte vertical.
```
overflow-x: auto;
```
```
overflow-y: hidden;
```

***

### Redefinindo as Propriedades Padrões dos Navegadores

Agora, vamos ver como configurar o nosso CSS de forma a padronizar a estilização em todos os navegadores. 

Para isso, vamos utilizar uma técnica chamada **reset.css**. Essa técnica consiste em criar um outro arquivo CSS para resetar a configuração padrão dos navegadores.

Você também pode utilizar um reset pronto como o Eric Mayer: [Clique aqui!](https://meyerweb.com/eric/tools/css/reset/)

Vamos criar um arquivo reset CSS e aplicar o seguinte código:

```
* {
    padding: 0;
    margin: 0;
    vertical-align: baseline;
    list-style: none;
    border: 0;
}
```

Veja que acabamos de resetar o que precisamos por conta própria. Você pode resetar mais coisas se precisar.

Para usar o código acima execute os seguintes passos.
* Você cria um arquivo reset.css;
* Adicione os comando de reset;
* Acha o arquivo css principal;
* E usa a regra css ```@import url('reset.css')```;