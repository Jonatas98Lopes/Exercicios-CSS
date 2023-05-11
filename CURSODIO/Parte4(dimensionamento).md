# Fundamentos do CSS


## Dimensionamento e Espaçamento

### Largura e Altura

Nomes temos duas propriedades para alterar dimensionamente de elementos.

* **width**: para alterar largura. Geralmente a unidade de medida referência aqui é o pixel.
```
width: 200px;
```
Podemos colocar em ambos, altura e largura, três valores especiais. O **auto** que define um valor automático para a propriedade, o valor **initial** que usará o valor padrão da propriedade o valor **inherit** que fará com que o elemento selecionado herde a altura ou largura de seu pai. 

* **height**: para alterar altura. Geralmente a unidade de medida referência aqui é o pixel.
```
height: 200px;
```

***

### Largura e Altura Máxima e Mínima

Nós podemos definir mínimo e máximo para largura ou altura de nossos elementos HTML através das seguinte propriedades CSS.

Mínima largura: Mesmo que o conteúdo do elemento seja menor que 100px, Esta será a largura mínima.
```
min-width: 100px;
```
Máxima largura: Mesmo que o conteúdo do elemento seja maior que 700px, Esta será a largura máxima.
```
max-width: 700px;
```
Mínima altura: Mesmo que o conteúdo do elemento seja menor que 300px, Esta será a altura mínima.
```
min-height: 300px;
```
Máxima altura:Mesmo que o conteúdo do elemento seja amior que 500px, Esta será a altura máxima.
```
max-height: 500px;
```

***

### Margin

**Tudo que está sendo falado aqui pode ser visto através do DevTools ou Inspetor de Elementos.**

Em português, margem. Esta propriedade define um espaçamento por FORA do nosse elemento HTML.

Nosso elemento pode possuir margem em todos os seus quatro lados. Em cima, embaixo, direita ou esquerda. Para cada um dos lados, temos um síntaxe:

Margem em cima do elemento:
```
margin-top: 500px;
```
Margem embaixo do elemento:
```
margin-bottom: 300px;
```
Margem à direita do elemento:
```
margin-right: 30px;
```
Margem à esquerda do elemento:
```
margin-left: 90px;
```
Mas... E se eu quiser definir um valor padrão para todos os lados? Basta usar apenas **margin** no nome da propriedade e o valor da propriedade será atribuído para todos os lados.
```
margin: 10px;
```
E se eu aplicar dois valores nesta propriedade? Ele aplicará o **primeiro valor em cima e embaixo** da margem e o **segundo**, **na direita e esquerda**.

```
margin: 10px 20px;
```

E se eu aplicar três valores nesta propriedade? Ele aplicará o **primeiro valor em cima**, **o segundo, na direita e esquerda** e o **terceiro**, **embaixo**.
```
margin: 10px 20px 15px;
```

E se eu aplicar quatro valores nesta propriedade? Ele aplicará o **primeiro valor em cima**, **o segundo, na direita**,o **terceiro**, **embaixo** e o quarto, **na esquerda**.
```
margin: 10px 20px 15px;
```
Não há como colocar mais valores.

Você pode também aplicar valores negativos, fazendo com que o elemento recue para o lado que foi definido.
```
margin-right: -40px;
```
Você pode usar o valor especial **inherit** para herdar a margem do pai.
 
Ou usar a palavra reservada **auto**. Se você usar auto, ele vai calcular a largura do nosso elemento, a largura restante da tela, e dividir essa largura restante da tela à esquerda e à direita do nosso elemento fazendo com que ele fique **centralizado**.
```
margin: 20px auto;
```

***

### Padding

O padding é o espaçamento DENTRO do nosso elemento HTML. Em outras palavras, quando nós aplicamos padding, nós separamos o nosso elemento de seu conteúdo.

Você pode utilizálo do mesmo jeito que **margin**, ou seja:

Padding em cima do elemento:
```
padding-top: 500px;
```
Padding embaixo do elemento:
```
padding-bottom: 300px;
```
Padding à direita do elemento:
```
padding-right: 30px;
```
Padding à esquerda do elemento:
```
padding-left: 90px;
```
Padding igual para todos os lados do elemento.
```
padding: 10px;
```
Padding em cima e embaixo de 10px, à direita e à esquerda, 20px.
```
padding: 10px 20px;
```
Padding em cima de 10px, à direita e à esquerda, 20px e embaixo, 15px.
```
padding: 10px 20px 15px;
```
Padding em cima de 10px, à direita, 20px, embaixo, 15px e à esquerda, 25px.
```
padding: 10px 20px 15px 25px;
```
Padding negativo fazendo com que o elemento recue. No caso, recua para a direita 40px
```
padding-right: -40px;
```
Padding auto que centraliza o elemento na horizontal.
```
padding: auto;
```

Lembre-se: Sempre que você aumenta o padding, você está aumentando a largura ou altura do elemento junto. Isso acontece porque a largura é defina pela fórmula: **largura = largura + borda + padding**. O mesmo acontece para a altura, **altura = altura + borda + padding**.

Na próxima seção, veremos como alterar isso.
***

### Box Sizing

O box-sizing serve justamente para alterar o comportamento da largura padrão ou altura padrão das propriedades **width** e **height**, fazendo com que aquela fórmula anterior seja quebrada e só seja levada em conta a largura ou altura passadas no width ou height.

Essa propriedade aceita dos valores:

* **content-box**
```
box-sizing: content-box;
```

É justamente o valor padrão. Ou seja o **width** do elemento será calculado pela fórmula *width = largura + borda + padding*.

* **border-box**
```
box-sizing: border-box;
```
Neste caso, o programa será obrigado a respeita o **width** estabelecido. Para isso ele vai diminuir a largura ou altura do **conteúdo** de forma automática se for preciso para que o **width** ou **height** definidos sejam respeitados.