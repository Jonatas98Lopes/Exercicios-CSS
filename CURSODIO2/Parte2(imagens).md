# Apresentação à Estilização Básica com CSS

## Imagens

Nesta seção, vamos estudar 2 propriedades que serão fundamentais para trabalharmos com imagens ou vídeo no nosso CSS.

### Propriedades Object-Fit

Object-Fit significa: **Ajuste de Elemento**.

Essa propriedade determina como imagens ou vídeo serão redimensionados de forma que caibam dentro da caixa do nosso elemento ou container.

Ela decide se a proporção de uma imagem, ou vídeo, deve ser preservada dentro do container ou não. 

Existem alguns valores para essa propriedade:
   
   * **fill(padrão)**: Fará com que a imagem seja esticada para preencher todo container da tag **img**.
```
img {
    object-fit: fill;
}
```
   Esse é o valor padrão da propriedade, então se você não informar nada, ele será o escolhido.

   * **contain**: Ela vai redimensionar a imagem similar quando redimensionamos uma foto segurando **shift** e arrastando ela pelos cantos da imagem, fazendo que a **largura** da imagem seja contida dentro do container. 
```
img {
    object-fit: contain;
}
```
   * **cover**: Funciona similar à **fill**, ou seja, ela faz a imagem cobrir todo o container, porém, não distorce a imagem. Esse valor redimensiona a imagem como **contain** e aproxima a imagem também se for preciso.
```
img {
    object-fit: cover;
}
```

   * **none**: Como o próprio nome diz, ela não altera proporção da imagem mesmo! De forma que se eu tenho uma imagem maior que o container do elemento, essa imagem será mantida na sua proporção, porém, só aparecerá a parte que é possível mostrar no elemento devido à imagem ser maior. 
```
img {
    object-fit: none;
}
```

   * **scale-down**: Ele vai comparar entre os valores **contain** e **none** para ver qual terá uma exibição maior. Quando digo exibição melhor, estou falando qual dos dois apresentará uma imagem menos distorcida e mostrando mais partes da imagem. Geralmente, escolhe o valor que mostra uma imagem menor.
```
img {
    object-fit: scale-down;
}
```
***

### Propriedades Object-Position

Essa propriedade é utilizada juntamente com **object-fit**.Ela serve para posicionar as imagens ou vídeos dentro do container.

O valor padrão dessa propriedade é:
```
img {
    object-position: 50% 50%;
}
```

Ou seja, por padrão, a imagem vem centralizada, pois o primeiro valor da propriedade cuida do posicionamento horizontal da imagem, eixo **x**, e o outro, do vertical, eixo **y**.

Nós também podemos usar outras unidades de medidas aqui como pixels.

```
img {
    object-position: 120px 250px;
}
```
É importante ressaltar que você pode usar valores negativos, e para isso, você deve entender o seguinte:

eixo **x**: Quando você coloca valores positivos, a imagem anda para a direita. Do contrário, anda para esquerda.

eixo **y**: Quando você coloca valores positivos, a imagem anda para baixo. Do contrário, anda para cima.

Exemplo:

```
img {
    object-position: -90px -25px;
}
```
No exemplo acima, estamos dizendo que a imagem deve andar 90px para a esquerda e 25 para cima.

Além disso, a gente pode usar as palavras reservadas: **left**, **right**, **center**, **top** e **bottom**

* **left**: Você só pode usar essa palavra no primeiro valor da propriedade. Ela vai empurrar a imagem para a direita, de forma que a esquerda da imagem apareça.
```
img {
    object-position: left 23px;
}
```
* **right**: Você só pode usar essa palavra no primeiro valor da propriedade. Ela vai empurrar a imagem para a esquerda, de forma que a direita da imagem apareça.
```
img {
    object-position: right 23px;
}
```
* **center**: Você pode usar essa palavra em ambos os valores. Fará que a imagem fique posicionada no centro horizontal ou vertical.
```
img {
    object-position: center 23px;
}
```
```
img {
    object-position: 23px center;
}
```
```
img {
    object-position: center center;
}
```
* **top**: Você só pode usar essa palavra no segundo valor da propriedade. Ela vai empurrar a imagem para a baixo, de forma que a parte de cima da imagem apareça.
```
img {
    object-position: 25px top;
}
```
* **bottom**: Você só pode usar essa palavra no segundo valor da propriedade. Ela vai empurrar a imagem para cima, de forma que a parte de baixo da imagem apareça.
```
img {
    object-position: 25px bottom;
}
```

Existem valores **start** e **end** não explicados.