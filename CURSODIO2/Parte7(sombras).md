# Apresentação à Estilização Básica com CSS

## Sombras

Nesta seção, vamos aprender como definir sombras nos nossos elementos.

### Efeito de Sombra nos Elementos

Vamos confessar vendo a propriedade **box-shadow**. Essa propriedade nos permite adicionar uma sombras do lado direito e embaixo do elemento. Esses valores definimos através de dois valores, normalmente em pixels, numéricos.

Exemplo: O primeiro valor se refere a sombra à direita e o segundo, à que está embaixo do elemento.

```
box-shadow: 10px 30px;
```

Podemos também adicionar valores negativos. Isso alterará a direção da sombra. 

Exemplo:
```
box-shadow: -12px -30px;
```
Isso fará com que a sombra fique 12px à esquerda e 30px, da parte superior do elemento.

Além disso, se quisermos alterar a cor da nossa sombra, basta adicioná-la ao depois do segundo valor numérico.

Exemplo:
```
box-shadow: 10px 30px red;
```

Porém se quisermos desfocar essa sombra, basta adicionar um terceiro valor numérico depois dos valores da sombra.

Exemplo: O primeiro valor se refere a sombra à direita, o segundo, à que está embaixo do elemento, o terceiro, ao grau de des  foque e o quarto, a cor da sombra.

```
box-shadow: 10px 30px 10px red;
```

Quanto maior o terceiro número, maior o número de desfoque.

Se adicionarmos um quarto valor numérico, controla a propagação da sombra ao longo  de sua espessura
```
box-shadow: 10px 30px 10px -7px red;
```

Se a gente quiser que a sombra fique por dentro do elemento, ao invés de por fora, basta adicionar o valor **inset** antes dos valores numéricos. 
```
box-shadow: inset 10px 30px 10px -7px red;
```
Isso também faz com que a sombra gire 180 graus, ou seja, agora a sombra está ao lado esquerdo do elemento e na parte superior dele também.

Além disso, podemos criar várias camadas de sombra.
```
box-shadow: inset 10px 30px 10px -7px red, 15px 15px 10px black;
```

A vírgula separa as camadas de sombra do nosso elemento.

Outra curisiodade. Se você estiver trabalhando com **imagens**, e quiser utilizar sombras dentro da imagem e não por fora do container, utilize a propriedade **filter** juntamente com a função **drop-shadow**. 
```
filter: drop-shadow(inset 10px 30px 10px -7px red);
```
A definição de valores funciona exatamente como **box-shadow**.

***

### Efeito de Sombra nos Textos

Agora, vamos ver a propriedade **text-shadow**. Como vimos anteriormente, conseguimos adicionar sombra aos nossos elementos através da propriedade **box-shadow**. **text-shadow** faz o mesmo para textos apenas.
```
text-shadow:  10px 30px 10px -7px red;
```
A configuração de valores é idêntica ao **box-shadow**, porém, não podemos adicionar o valor **inset** aqui.
