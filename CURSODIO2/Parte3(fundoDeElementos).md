# Apresentação à Estilização Básica com CSS

## Fundo dos Elementos
Vamos ver todas as formas de manipular o fundo dos elementos nesta seção.

### Alterando o Fundo dos Elementos
Nós podemos usar uma propriedade chamada **background-image** para alterar os fundo dos nossos elementos de duas formas:

* **Inserir uma imagem de fundo**:

Exemplo:
```
div {
    background-image: url(../images/minha_fot.jpg);
}
```
***
* **Inserir uma cor gradiente**:


Você pode adicionar quantas cores quiser nelas.

Um gradiente linear:

```
div {
    background-image: linear-gradient(lightgreen, lightblue);
}
```
Um gradiente radial:

```
div {
    background-image: radial-gradient(lightgreen, lightblue);
}
```
Um gradiente linear que repete:

```
div {
    background-image: repeating-linear-gradient(to top, lightgreen,0 20px, lightblue, 0 20px);
}
```
Um gradiente radial que repete:

```
div {
    background-image: repeating-radial-gradient(to top, lightgreen,0 20px, lightblue, 0 20px);
}
```
Site de Texturas Coloridas: [Clique aqui!](https://projects.verou.me/css3patterns/)

Além disso eu posso criar várias camadas de fundos com o background-image. Vamos ver um exemplo:
```
div {
    background-image: linear-gradient(lightgreen, lightblue),  url(../images/minha_fot.jpg);
}
```

Veja que temos uma foto e um gradiente como fundos, porém, a foto é a segunda camada do fundo(A CAMADA MAIS EMBAIXO) e é declara depois, e o gradiente é a primeira camada(A CAMADA MAIS EM CIMA) e é o valor mais próximo da propriedade, ou seja, o gradiente vai sobrepor a imagem.

***

### Redimensionando as Imagens de Fundo dos Elementos

Nós já aprendemos a redimensionar fotos e vídeos que estão dentro das tags: **img** e **video**

Agora, vamos aprender a fazer o mesmo com as imagens de fundos do nosso CSS atráves da propriedade **background-size**.

Primeiramente, essa propriedade pode receber algumas palavras chaves como valores:

* **auto(padrão)**: É o valor padrão da propriedade. Fará a foto se ajustar automaticamente ao container. Geralmente, ela vai do canto superior esquerdo da imagem de fundo até cobrir todo o elemento, ou se a imagem for menor, fará ela se repetir.

```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: auto;
}
```
* **cover**: Fará a imagem cobrir todo o container. Se a imagem for menor do que o container, ele aproxima ela.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: cover;
}
```
* **contain**: Redimensiona a imagem horizontalmente, de forma que a largura da imagem seja contida dentro da imagem sem distorcer.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: contain;
}
```

Além disso, podemos usar valores numéricos em pixels, porcentagens, etc...

Nós podemos passar um valor numérico para essa porcentagem. Isso significa que estamos ajustando apenas a largura, porém, como em tudo no CSS, quando você ajusta a largura de uma imagem, a altura é ajustada de forma automática para não distorcer o elemento.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 240px;
}
```
Se o valor passado for igual ao tamanho do container, a imagem toma o espaço inteiro, se for menor, a imagem ocupará aquele espaço determinado e começará a se repetir. Se for maior, a imagem será cortada.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 100%;
}
```
O valor 100% significa que a imagem vai tomar todo o espaço do container.

Porém, podemos ajustar a altura da imagem adicionando o segundo valor numérico a propriedade, mas CUIDADO. Você pode distorcer ela.

```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 240px 240px;
}
```
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 100% 100%;
}
```

Se você tiver mais imagens de fundo no seu elemento, você pode separar por vírgulas os valores de cada imagem, começando da primeira camada até a última.
```
div {
    background-image: url(./assets/fotoExemplo2.png), url(./assets/fotoExemplo.png);
    background-size: 100% 100%, 50% 50%;
}
```
Isso significa que a largura e altura de 100% são da imagem da primeira camada. Já a largura e altura de 50% são da imagem de segunda camada, pois está depois da vírgula.
```
div {
    background-image:  url(./assets/fotoExemplo2.png), url(./assets/fotoExemplo.png);
    background-size: contain, cover;
}
```
Isso significa que o valor contain pertence a imagem de primeira camada. Já cover, pertence a segunda camada, pois está após a vírgula.
***

### Repetição das Imagens de Fundo

Como vimos anteriormente, independetemente do valor que colocássemos no **background-size**, se a imagem fosse menor do que o container, ela começava a se repetir por padrão. Na aula de hoje, vamos ver como configurar isso.

Nós vamos usar a propriedade **background-repeat** para configurar a repetição das imagens. Ela aceita os seguinte valores:

* **repeat(padrão)**: Esse valor é padrão e é o que aconteceu nos exemplos das aulas anteriores. Ele faz com que a imagem se repita tanto na horizontal como na vertical. 
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: repeat;
}
```
* **repeat-x**: Esse valor faz com que a imagem só se repita no eixo horizontal, caso a imagem seja menor do que o container. 
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: repeat-x;
}
```
* **repeat-y**: Esse valor faz com que a imagem só se repita no eixo vertical, caso a imagem seja menor do que o container. 
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: repeat-y;
}
```
* **space**: Esse valor permite a imagem se repetir tanto na horizontal como na vertical, assim como o valor padrão, **repeat**. Porém ele não permite que as imagens sejam cortadas. Para isso, ele adiciona um espaço automático no meio do container na medida em que um das repetições das imagens seria cortada.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: space;
}
```
* **round**: Faz com que a imagem se repita igual à **repeat**. Porém, redimensiona a imagem para que as repetições caibam perfetamente dentro do container sem haver cortes.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: round;
}
```
* **no-repeat**: Impede a repetição  de imagem caso ela seja menor que o container.
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: no-repeat;
}
```

Além disso, você pode aplicar dois desse valores na propriedade. Se esses dois valores forem iguais, não há necessidade de adicionar um segundo valor. 
```
div {
    background-image: url(./assets/fotoExemplo.png);
    background-size: 260px;
    background-repeat: space, no-repeat;
}
```
Neste caso, estou adicionando o valor space para o eixo horizontal e no-repeat, para o vertical.

### Posicionamento das Imagens de Fundo
Depois de aprender a adicionar uma imagem de fundo, definir seu tamanho, definir se ela vai se repetir caso for menor, agora vamos ver como posicionar essa imagem de fundo na tela

Para uma imagem comum, nós apenas usaríamos o **object-position**. Porém, estamos trabalhando com imagens de fundo. Vamos ver isso agora.

Nós vamos usar a propriedade **background-position**. Ela possui diversos valores. E nós podemos definir dois valores para ela, o valor do eixo x e o do eixo y:

Vamos ver algumas formas de definir isso:

* **bottom**: Define que a imagem vai ficar na parte inferior do container.
* **top**: Define que a imagem vai ficar na superior do container.
* **right**: Define que a imagem vai ficar à direita do container.
* **bottom**: Define que a imagem vai ficar à esquerda do container.
* **center**: Define que a imagem vai ficar ao centro da imagem seja ele horizontal ou vertical.

Exemplo:
```
p {
    background-image: url(./assets/imagem.png);
    background-position: right bottom;
}
```

Neste caso, estamos dizendo que a imagem vai ficar à direita e na parte inferior da imagem, pois o primeiro valor define a posição da imagem no eixo x e o segundo, no eixo y.

Além disso, podemos passar valores em pixels, porcentagem, etc.
Exemplo:
```
p {
    background-image: url(./assets/imagem.png);
    background-position: 25px 100%;
}
```
Acima, definimos que a imagem vai andar 25 pixels para a direita e vai ficar encostada na parte inferior da imagem.

Podemos passar só um valor para a propriedade

Exemplo:

```
P {
     background-image: url(./assets/imagem.png);
    background-position: bottom;
}
```
Neste caso, como estamos alterando APENAS o eixo-y da imagem, por padrão o CSS definirá o eixo-x como **center**.

Você também pode definir isso para múltiplas camadas de fundo. Assim como nas outras propriedades desta seção.

***

### Propriedade Background Attachment
Essa propriedade vai definir como o fundo do elemento(imagem) vai se comportar quando nós arrastarmos a barra de rolar do navegador. O nome da propriedade é **background-attachment**.

Nós podemos ter 3 valores para ela.

* **fixed**: Se o elemento que contém ela tiver uma barra de rolagem própria, a imagem fica fixa quando usamos esta barra de rolagem. Porém, quando rolamos a barra de rolagem da página inteira, faz com que a imagem vai desaparecendo aos pouco quandos rolarmos a página para baixo
```
background-attachment: fixed; 
```
* **scroll**:Se o elemento que contém ela tiver uma barra de rolagem própria, a imagem fica fixa quando usamos esta barra de rolagem. Porém, quando rolamos a barra de rolagem da página inteira, faz com que a imagem suma junto com a barra de rolagem. Esse é o feito mais comum que temos
```
background-attachment: scroll; 
```
* **local**: Se o elemento que contém ela tiver uma barra de rolagem própria, a imagem vai rolar junto com o conteúdo do elemento quando usamos esta barra de rolagem. Porém, quando rolamos a barra de rolagem da página inteira, faz com que a imagem fique fixa igual ao **scroll**.
```
background-attachment: local; 
```
***

### Propriedade Background Origin
Vamos ver a propriedade **background-origin** agora. Ela define qual o ponto de origem de uma imagem de fundo.

Essa propriedade possui os possíveis valores:

* **padding-box(padrão)**: A imagem de fundo vai iniciar do canto superior esquerdo do nosso **padding**.
```
background-origin: padding-box; 
```

* **border-box**: A imagem de fundo vai iniciar do canto superior esquerdo da nossa **borda**.
```
background-origin: border-box; 
```

* **content-box**: A imagem de fundo vai iniciar do canto superior esquerdo do nosso **conteúdo**.

```
background-origin: border-box; 
```
***

### Propriedade Background Clip

Essa propriedade é quase idêntica à anterior, porém, ela permite que apliquemos as funcionalidades de background-origin para cores de fundo sólidas também, além de poder aplicar um valor à mais para colocar o fundo somente no conteúdo do elemento. O nome dessa propriedade é **background-clip**.

* **padding-box(padrão)**: A imagem de fundo vai iniciar do canto superior esquerdo do nosso **padding**.
```
background-clip: padding-box; 
```

* **border-box**: A imagem de fundo vai iniciar do canto superior esquerdo da nossa **borda**.
```
background-clip: border-box; 
```

* **content-box**: A imagem de fundo vai iniciar do canto superior esquerdo do nosso **conteúdo**.
```
background-clip: content-box; 
```
* **text**: Permite que coloquemos o fundo só no texto do elemento.
```
webkit-background-clip: text;
color: transparent;
background-clip: text; 
```
Você irá notar que só texto teve o background. Mas para usar este comando nós tivemos que usar outras duas linhas anteriores. 

Tivemos que usar a linha **webkit**. Ela serve para que Chrome permita a utilização da propriedade.

Tivemos que tornar a cor do texto transparente, para que a cor do fundo se sobresaia.
***

### Mesclagem

Essa propriedade permite que nós misturemos as imagens de fundo do elemento com as cores de fundo. O nome dessa propriedade é **background-blend-mode**.

Ela aceita os seguintes valores:

* **normal(padrão)**: Valor padrão

* **multiply**: Mescla as cores.
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: multiply;
}
```
Ela vai misturar a cor de fundo com a imagem de fundo.

* **sreen**: Deixa com mais brilho.
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: screen;
}
```
* **overlay**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: overlay;
}
```
* **darken**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: darken;
}
```
* **lighten**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: lighten;
}
```
* **color-dodge**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: color-dodge;
}
```
* **color-burn**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: color-burn;
}
```
* **hard-light**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: hard-light;
}
```
* **soft-light**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: soft-light;
}
```
* **difference**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: difference;
}
```
* **exclusion**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: exclusion;
}
```

* **hue**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: hue;
}
```
* **saturation**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: saturation;
}
```
* **color**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: color;
}
```
* **luminosity**: 
```
div {
    background-color: red;
    background-image: url(./assets/images/foto.png);
    background-blend-mode: luminosity;
}
```
Todos esses valores devem ser testados. Não há muito do que ser explicado aqui. Apenas teste!

Você pode testar esses valores antes de usar usando o site a seguir: [Clique aqui!](https://codepen.io/team/css-tricks/pen/GgavOP?editors=1100)


***

### Propriedade Background
Aqui nós vamos explorar a propriedade **background**. Como nós já vimos praticamente tudo o que é possível fazer com o as propriedades background, vamos entender essa também.

A propriedade background nada mais é do que um atalho para todas as outras. Ou seja, eu posso definir todas as outras propriedades de background de elementos CSS através dela. O que vai determinar a que tipo de propriedade eu estou me é a ordem na qual eu insiro os valores.

Exemplo:
```
background: url(./assets/image/foto.png) /* background-image*/
top center /* background-position/ background-size*/
no-repeat /* background-repeat*/
fixed /* background-attachment */
padding-box /* background-origin */
content-box /* background-clip */
red /* backgrond-color */;
```
Muito cuidado ao usar este tipo de síntaxe. Algumas propriedades sobrescrevem outras, como no caso de você definir um background-color antes de um background. Não funcionará. Tente sempre usar nomes de propriedades específicas.
