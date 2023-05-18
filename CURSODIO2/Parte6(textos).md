# Apresentação à Estilização Básica com CSS

## Textos

Agora, vamos olhar as propriedades que nos permitem estilizar os textos da nossa página.


### Propriedade Text-Transform

Nesta primeira aula, vamos ver a propriedade **text-transform**. Essa propriedade é responsável por definir quais caracteres vão ficar em maiúsculo ou minúsculo.

Essa propriedade aceita alguns valores:

* **none(padrão)**: É o valor padrão. Esse valor diz para o CSS manter o texto como foi digitado no HTML.
```
text-transform: none;
```
* **capitalize**: Esse valor transformará o primeiro caractere de todas as palavras do texto em maiúsculo. Os outros caracteres serão mantidos como foi digitado.
```
text-transform: capitalize;
```
* **uppercase**: Transforma todos os caracteres do texto em maiúsculo.
```
text-transform: uppercase;
```
* **lowercase**: Transforma todos os caracteres do texto em minúsculo.
```
text-transform: lowercase;
```

Além disso, essa propriedade aceita outros 2 valores:

* **initial**: Toda vez que você passa o valor **initial** numa propriedade, significa que o valor inicial da propriedade será usado, ou seja, o valor padrão, no caso, esse valor é **none**.
```
text-transform: initial;
```
* **inherit**: Ela vai herdar o valor dessa propriedade do elemento pai.
```
text-transform: inherit;
```
***

### Propriedade Text-Align

Agora, vamos ver a propriedade **text-align**. Essa propriedade é responsável por alinhar o nosso texto na **horizontal**, dentro do elemento que o contém.

Essa propriedade aceita alguns valores:

* **left(padrão)**: Esse é o valor padrão. Alinha o nosso texto à esquerda.
```
text-align: left;
```
* **right**: Alinha o nosso texto à direita.
```
text-align: right;
```
* **center**: Alinha o nosso texto ao centro horizontal do elemento.
```
text-align: center;
```
* **justify**: Alinha o nosso texto de forma justificada, ou seja, o texto ocupará todo espaço horizontal de todas as linhas do texto, exceto a última linha.
```
text-align: justify;
```

Estes são os principais valores desta propriedade.

***

### Propriedade Text-Decoration

Agora, vamos ver a propriedade **text-decoration**. Essa propriedade pode adicionar ou remover linhas do nosso texto. As linhas podem estar em cima, no meio, ou embaixo do texto.

Essa propriedade aceita os seguintes valores:

* **none(padrão)**: Não é adiciona linhas ou removido linhas do texto.
```
text-decoration: none;
```
* **underline**: Será adicionado uma linha embaixo do texto, o famoso efeito de **sublinhado** será aplicado.
```
text-decoration: underline;
```
OBS: A TAG **a** DO HTML VEM COM O VALOR PADRÃO DE ```text-decoration: underline;``` AJUSTADO. EM OUTRAS PALAVRAS, SE QUISERMOS TIRAR O SUBLINHADO DESSA TAG, PRECISAMOS AJUSTAR O TEXT-DECORATION DELA DESTA FORMA: ```text-decoration: none;```

* **line-through**: Será adicionado uma linha no meio do texto, o famoso efeito de **riscado** será aplicado.
```
text-decoration: line-through;
```
* **overline**: Será adicionado uma linha em cima do texto.
```
text-decoration: overline;
```

Porém essa propriedade é considerada uma abreviação e junção de outras 4 propriedades. São elas:

* **text-decoration-line**: Ela específica para determinar o tipo de linha que será adicionada. Então, todos os valores que acabamos de ver para **text-decoration** são válidos aqui.
Valor padrão:
```
text-decoration-line: none;
```
```
text-decoration-line: underline;
```
```
text-decoration-line: line-through;
```
```
text-decoration-line: overline;
```
* **text-decoration-style**: Essa propriedade define o estilo da linha defina em **text-decoration-line**:
   * **solid(padrão)**: O valor padrão. Cria uma linha contínua.
   ```
   text-decoration-style: solid;
   ```
   * **double**: Cria uma linha dupla.
   ```
   text-decoration-style: double;
   ```
   * **dotted**: Cria uma linha pontilhada.
   ```
   text-decoration-style: dotted;
   ```
   * **dashed**: Cria uma linha traçada, com vários traços.
   ```
   text-decoration-style: dashed;
   ```
   * **wavy**: Cria uma linha em formato de ondas.
   ```
   text-decoration-style: wavy;
   ```
* **text-decoration-color**: Essa propriedade define a cor da nossa linha. Se você não informar a cor da linha, ela vai seguir a cor do nosso texto.
```
text-decoration-color: red;
```
* **text-decoration-thickness**: Ela define a espessura da linha que estamos criando nos nossos textos. Ela aceita várias unidades de medidas. incluindo pixels.
```
text-decoration-thickness: 5px;
```

Como mencionado, **text-decoration** é uma abreviação de todas essas propriedades. Portanto, podemos definir todos esses valores dentro dela.

Exemplo:
```
text-decoration: underline solid red 1px;
```
Então, se quisermos definir todos esses valores dentro de **text-decoration**, passamos os valores na seguinte ordem: o tipo da linha, o estilo da linha, a cor da linha e a espessura da linha.
***

### Propriedade Text-Ident

Agora, vamos ver a propriedade **text-ident**. Essa propriedade faz com que a primeira linha do nosso texto tenha um espaço antes dela. Esse espaço representa um parágrafo e a quantidade de espaços é você que define.

Essa propriedade aceita diversos tipos de valores incluindo valores em pixels e valores negativos.

```
text-ident: 10px;
```
O texto começará 10px avançado para a direita.
```
text-ident: -10px;
```
O texto começará 10px adiantado à esquerda.

***

### Propriedade Letter-Spacing e Word-Spacing

Agora, vamos a propriedade **letter-spacing**. Essa propriedade vai adicionar um espaçamento entre cada CARACTERE do seu texto.

O valor padrão dessa propriedade é **normal**:
```
letter-spacing: normal;
```

Porém você pode usar valores positivos em pixel, o que fará o espaçamento entre os caracteres aumentar:
```
letter-spacing: 12px;
```
Ou valores negativos, o que fará o espaçamento entre os caracteres diminuir.
```
letter-spacing: -17px;
```


Da mesma forma, nós temos a propriedade **word-spacing**. Essa propriedade vai adicionar um espaçamento entre cada PALAVRA do seu texto.

O valor padrão dessa propriedade é **normal**:
```
word-spacing: normal;
```

Porém você pode usar valores positivos em pixel, o que fará o espaçamento entre as palavras aumentar:
```
word-spacing: 12px;
```
Ou valores negativos, o que fará o espaçamento entre as palavras diminuir.
```
word-spacing: -17px;
```

***

### Propriedade White-Space

Agora, veremos a propriedade **white-space**. Essa propriedade altera o comportamento dos espaços em brancos do nosso texto.

Essa propriedade aceita os seguintes valores: 

* **normal(padrão)**: Esse valor faz que os espaços em branco sejam apenas de uma unidade entre cada palavra. Se você colocar 4 espaços em branco entre duas palavras, por exemplo, esses espaços serão convertidos em 1. Além disso, se houver quebrar de linhas no texto HTML, elas serão completamente ignoradas.
```
white-spacing: normal;
```
* **nowrap**: Esse valor faz quase a mesma coisa que o valor **normal**, porém, o nosso texto nunca é quebrado, mesmo quando alcança o final do container do elemento. Isso faz com que todo o texto fique em uma linha só.
```
white-spacing: nowrap;
```
* **pre**: Esse valor respeita totalmente as quebras de linhas e os espaços em brancos. Em outras palavras, seu textos será exibido exatamente como você digitou.
```
white-spacing: pre;
```
* **pre-line**: Esse valor converte todos os espaços em branco entre palavras em 1, quebra linha se o conteúdo do texto alcançar o fim do container do elemento ou se você der uma quebra de linha.
```
white-spacing: pre-line;
```
* **pre-wrap**: Esse valor respeita os espaços em branco que você definir, quebra o texto quando ele alcançar o limite do container e também quebra o texto nas quebras de linha que você definir.
```
white-spacing: pre-wrap;
```
* **break-spaces**: Esse valor faz o mesmo que **pre-wrap**, ou seja, respeita os espaços em branco que você definir, quebra o texto quando ele alcançar o limite do container e também quebra o texto nas quebras de linha que você definir, porém  a diferença é que se você colocar espaços em brancos que ultrapassem o largura do nosso container, ele vai quebrar esses espaços, diferentemente de pre-wrap. Em pre-wrap, se você colocar muitos espaços em branco que ultrapassem o limite do container, esses espaços não são quebrados.
```
white-spacing: break-spaces;
```

***

### Propriedade Word-Wrap

Agora, vamos a propriedade **word-wrap**. Essa propriedade nos permite quebrar uma palavra, em qualquer caractere, caso ela exceda o limite do container.

Essa propriedade aceita 2 valores:

* **normal(padrão)**: Esse é o valor padrão. Se uma determinada palavra ultrapassar os limites do container, ela **NÃO** será quebrada. O texto só será quebrado na próxima palavra.
```
word-wrap: normal;
```
* **break-word**: Esse valor quebra a palavra exatamente no caractere necessário e coloca a segunda parte na linha debaixo.
```
word-wrap: break-word;
```

***

### Propriedade Word-Break

Agora, vamos ver a propriedade **word-break**. Essa propriedade nos permite mudar o comportamento padrão de quebra de linha do nosso CSS. 

Geralmente, o nosso navegador quebra linha num espaço em branco ou num hífen. Vamos aprender como alterar isso agora!

Essa propriedade aceita os seguintes valores:

* **normal(padrão)**: Esse é o valor padrão. Em outras palavras, ocorre exatamente como mencionamos acima. As quebras de linha ocorrem quando há um espaço em branco ou um hífen.
```
word-break: normal;
```
* **break-all**: Esse valor faz com que a palavra seja quebrada em qualquer caractere para que não ultrapasse o limite do container, parecido com ```word-wrap: break-word;```, mas há uma diferença. Quando você usa o ```word-wrap: break-word;```, o CSS identifica se a próxima palavra pode ser escrita por inteiro na linha sem ultrapassar os limites do container ou não. Já ```word-wrap: break-word;``` não. Ele não verifica isso. Ele quebra a próxima palavra em qualquer lugar.
```
word-break: break-all;
```
* **keep-all**: No chinês, japonês ou coreano, textos não podem ser quebrados em linhas diferentes. Quando você usa esse valor, ele verifica o idioma do texto e caso ele seja um desses três, ele mantém a linha até o fim.
```
word-break: keep-all;
```

***

### Propriedade Writing-Mode

Agora, vamos ver a propriedade **writing-mode**. Essa propriedade define se o texto deve ser lido do topo para baixo, como no chinês(VERTICAL), ou da esquerda para a direita, como no português ou inglês(HORIZONTAL).

Essa propriedade aceita 3 valores: 

* **horizontal-tb(padrão)**: Esse é o valor padrão. Faz com que o fluxo do texto seja da esquerda para a direita e a próxima linha sempre estará posicionada abaixo da anterior.
```
writing-mode: horizontal-tb;
```
* **vertical-rl**: Esse valor faz com que o nosso texto flua na vertical. O texto fica deitado, a leitura começa da direita e a próxima linha será adicionada à esquerda da linha anterior.
```
writing-mode: vertical-rl;
```
* **vertical-lr**: Esse valor faz com que o nosso texto flua na vertical. O texto fica deitado, a leitura começa da esquerda e a próxima linha será adicionada à direita da linha anterior.
```
writing-mode: vertical-lr;
```

***

### Propriedade Text-Overflow

Por último, vamos ver a propriedade **text-overflow**. Essa propriedade nos permite definir como mostraremos o texto que excedeu o limite do container do elemento para o usuário.

Essa propriedade aceita alguns valores: 

* **clip(padrão)**: O texto simplesmente é cortado e nenhum elemento é adicionado ao fim do texto.
```
text-overflow: clip;
```
* **ellipsis**: Ele adiciona retincências ao fim do container mostrando para o usuário que há mais conteúdo a ler.
```
text-overflow: ellipsis;
```
* **string**: Neste caso, podemos digitar a mensagem que quisermos exibir ao usuário no final do container para mostra-lhe que há mais coisas a ler. PORÉM SÓ FUNCIONA NO **FIREFOX**.
```
text-overflow: "Tem mais coisas para ler.";
```
***
