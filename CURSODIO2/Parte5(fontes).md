# Apresentação à Estilização Básica com CSS

## Fontes

Vamos trabalhar com fontes agora. Configurar fonte significa escolher a letra que queremos usar. Isso está altamente relacionado com a **tipografia** do site.

Dentro da tipografia existe 6 **tipos genéricos** ou **grupo de fontes**, são elas:
* **Serif**: Fontes com traços nas pontas.
Exemplo de fontes assim:
   * Times New Roman;
   * Georgia;


![Exemplo de Fonte Serifada](./assets/serif.png "Exemplo de font serif")
* **Sans-Serif** Também conhecidas como fontes sem serifas.

Exemplo de fontes assim:
   * Arial;


![Exemplo de Fonte Não Serifada](./assets/n%C3%A3oserifada.png "Exemplo de font san-serif")
* **Display**: Também conhecidas como *enfeitadas* ou *comemorativas*. Usadas para textos curtos onde queremos chamar atenção no nosso site.

![Exemplo de Fonte Comemorativa](./assets/display.png "Exemplo de font display")
* **Handwriting**: Também conhecidas como *cursivas* ou *manuscritas*. A gente usa elas quando queremos que algo pareça que foi escrito à mão. Vai trazer uma sensação de **humanização** no que você está lendo.

![Exemplo de Fonte Escrita à Mão](./assets/handwriting.png "Exemplo de font handwriting")
* **Monospace**: São fontes onde todos os caracteres ocupam o mesmo espaço.

![Exemplo de Fonte de Espaço único entre as palavras](./assets/monospace.png "Exemplo de font monospace")


### Onde Encontrar Fontes Personalizadas?

Nós podemos encontrar fontes que queremos utilizando o [**Google Fonts**](https://fonts.google.com/). O Google Fonts é um catálogo aberto onde podemos baixar fontes totalmente de graça.

***

### Personalizando as Fontes do Nosso Site

Nesta aula, vamos aprender sobre a propriedade **font-family**. 

Essa propriedade nos permite definir uma fonte específica para o nosso projeto:

```
font-family: "Times New Roman";
``` 
CUIDADO! SE O NOME DA FONTE TIVER ESPAÇOS, COLOQUE TODO O NOME ENTRE AS ASPAS, CASO CONTRÁRIO, NÃO FUNCIONARÁ.

Ou uma família de fontes:

* Serif:
```
font-family: serif;
``` 
* Sans-serif:
```
font-family: sans-serif;
``` 
* Display:
```
font-family: fantasy;
``` 
* Handwriting:
```
font-family: cursive;
``` 
* Monospace:
```
font-family: monospace;
``` 

Além disso, você pode configurar fontes secundárias para determinado elemento. Isso é interessante porque o computador do usuário pode não conter as fontes que definimos e precisamos passar o fonte secundária.

Podemos configurar isso colocando o nome das fontes separadas por vírgulas.
```
font-family: Arial, "Times New Roman";
``` 

Podemos mesclar as fontes secundárias entre famílias de fontes e fontes específicas:
```
font-family: Arial, "Times New Roman", fantasy;
``` 

***


### Aplicando Fontes Personalizadas com @Font-Face

O que vimos na última aula é muito útil, porém, só conseguimos usar fontes que o computador do usuário tenha. Vamos ver como usar fontes externas através da regra CSS **@font-face**. Re

Para usar essa regra, é necessário que você faça o download da fonte ou família da fonte que deseja usar. Você pode fazer isso através do [**Google Fonts**](https://fonts.google.com/) de graça. Depois de descompactar o arquivo de download, adicione a fonte dentro do seu projeto.

Com tudo pronto, podemos usar a sintaxe da nossa regra CSS:
```
@font-face {
    font-family: "Nova Fonte";
    src: url(./assets/font1.ttf);
}

```

Uma regra CSS é composta de algumas propriedade específicas. No caso de **@font-face**, nós temos a propriedade **font-family**, que receberá o nome de fonte que você quiser como valor, e a propriedade **src**, que receberá o caminho da fonte que você passar através da função **url**.

Você pode utilizar uma fonte que você fez o download ou uma fonte online, apenas passe o link da fonte dentro da função **url** caso use uma fonte online.

Porém, ao fazer isso, nada acontecerá no seu CSS. Isso acontece porque o que fizemos foi somente adicionar uma nova fonte ao nosso CSS, mas não definimos qual ou quais elementos receberão aquela fonte para estilização.

Para usar fonte, basta utilizarmos a propriedade **font-family** no elemento que quisermos e passar o nome que definimos para a nossa fonte, no nosso caso, definios **Nova Fonte**. Exemplo:
```
p {
    font-family: "Nova Fonte";
}
```

Além disso, você pode usar a função **local** antes de **url** na regra **@font-face**. Neste caso, estamos dizendo para o navegador procurar a fonte no projeto primeiro e caso não a encontre, ele vai buscar online através do valor passado em **url**. Exemplo:
```
@font-face {
    font-family: "Nova Fonte";
    src: local(), url(./assets/font1.ttf);
}

```

Existem outras configurações que podemos utilizar também. Podemos definir mais um **@font-face** e dependendo do valor da propriedade **font-weight** que utilizarmos dentro dela, uma **@font-face** será utilizada ou outra.
```
@font-face {
    font-family: "Nova Fonte";
    src: locurl(./assets/font1.ttf);
    font-weight: normal;
}

@font-face {
    font-family: "Nova Fonte";
    src: url(./assets/font1.ttf);
    font-weight: bold;
}
```

Se o nosso elemento usar essa fonte, e definirmos **bold** na propriedade **font-weight**, o segundo **@font-face** será utilizado. Caso seja **normal** dentro de **font-weight**, será utilizado o primeiro **@font-face**.

***

### Aplicando Fontes Personalizadas com @import url()

Agora, vamos ver a nossa segunda regra CSS chamada **@import**. Essa é uma outra forma de importar uma fonte para o seu código CSS, porém, ela só é útil para fontes online.

Geralmente você pega o link de importação no Google Fonts.
Exemplo: 
```
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@1,500&display=swap');
```
No mesmo site, você tenha a opção de copiar uma tag **link** já configurada e colá-la em todas os templates que quiser usar. A desvantagem dessa abordagem é que você terá que fazer isso para todos os arquivos HTML que está estilizando.
***

### Alterando Tamanho das Fontes com Font-Size

Agora, vamos conferir como funciona a propriedade **font-size**. Ela determina o tamanho do nosso texto. 

Geralmente, a gente passa o valor dessa propriedade em pixels, como abaixo:
```
font-size: 20px;
```

Porém essa propriedade também aceita algumas palavra chaves, vamos conferir abaixo:

* **xx-small**: Texto pequeníssimo.
``` 
font-size: xx-small;
```
* **x-small**: Texto muito pequeno.
```
font-size: x-small;
```
* **small**: Texto pequeno.
```
font-size: small;
```
* **medium**: Texto médio.
```
font-size: medium;
```
* **large**: Texto grande.
```
font-size: large;
```
* **x-large**: Texto muito grande.
```
font-size: x-large;
```
* **xx-large**: Texto grandíssimo.
```
font-size: xx-large;
```

O tamanho de fonte que cada uma dessa palavras implementam depende do tamanho de fonte padrão do usuário.

Além disso nós temos outras duas palavras chaves aceita aqui:
* **smaller**: Ele torna o texto do elemento menor do que a tag pai do elemento.
```
font-size: smaller;
```
* **larger**: Ele torna o texto do elemento maior do que a tag pai do elemento.
```
font-size: larger;
```
***

### Estilos de Fonte(Font-Style)

Vamos ver agora a propriedade **font-style**. Essa propriedade define o estilo da fonte, geralmente variando entre itálico e normal. Ela aceita 3 valores:

* **normal(padrão)**: Esse é o valor padrão. A fonte será normal sem qualquer traço de itálico.
```
font-style: normal;
```
* **italic**: Faz com que o texto fica em itálico. As letras ficam inclinadas.
```
font-style: italic;
```
* **oblique**: Faz com que o texto tenha efeito similar ao itálico. Um pouco menos inclinadas. Porém, esse efeito é pouco suportado pelos navegadores.
```
font-style: oblique;
```
Essa propriedade procura a configuração pré-definida para cada um dos seus valores no font-face dela. Caso não haja uma regra para um de seus possíveis valores, o próprio navegador vai simular o efeito.


***

### Espessura das Fontes com Font-weight

Se a gente quiser controlar a espessura dos nossos textos, a gente usar a propriedade **font-weight**. Lembre-se que o efeito negrito nada mais é do que a espessura de um texto aumenta ao máximo, então se quisermos configurar esse efeito, usamos **font-weight**.

Essa propriedade procura a configuração pré-definida para cada um dos seus valores no font-face dela. Caso não haja uma regra para um de seus possíveis valores, o próprio navegador vai simular o efeito.

Essa propriedade aceita valores de 100 a 900.

Mínimo:
```
font-weight: 100;
```
Máximo:
Porém, nem todas as fontes suportam todos os valores. Ou seja, dependendo da fonte que você usar, pode ser que não haja diferença de espessura entre 200 e 300, por exemplo. CUIDADO!

Além disso, essa propriedade aceita algumas palavras chaves:
* **normal(padrão)**: É o valor padrão caso você não declare o valor da propriedade.
```
font-weight: normal;
```
* **bold**: Transforma o nosso texto em negrito. É o mesmo que você definir o valor **700**.
```
font-weight: bold;
```
* **lighter**: Faz com que a espessura do texto fique mais fina do que o do elemento pai.
```
font-weight: lighter;
```
* **bolder**: Faz com que a espessura do texto fique mais grossa do que o do elemento pai.
```
font-weight: bolder;
```
***

### Variação das Fontes com Font-variant

Agora, vamos a propriedade **font-variant**. Essa propriedade nos permite modificar os textos para que ficem em **versalete**, ou **small-caps** em inglês. Esse efeito transforma todos os caracteres em maiúsculo, porém ele ficam menores do que se estivessem normais.

Essa propriedade aceita 2 valores:

* **normal(padrão)**: Texto normal com caracteres maiores e menores e texto em caixa alta.
```
font-variant: normal;
```
* **small-caps**: Texto de caixa baixa com caracteres em maiúsculo. Os caracteres que você digitar em minúsculo, ficarão em maiúsculo também apenas menores.
```
font-variant: small-caps;
```
***

### Propriedade Font-Stretch

Vamos ver nessa aula a propriedade **font-stretch**. Essa propriedade faz com que o nosso texto fica mais apertado na horizontal ou mais esticado.

OBS: NEM TODAS AS FONTES VOCÊ SER ALTERADAS QUANDO VOCÊ USAR ESSA PROPRIEDADE. PARA QUE ELA POSSA SER UTILIZADA, AS CONFIGURAÇÕES DA FONTE DEVEM PERMITIR ISSO. NA VERDADE, A MAIORIA DAS FONTES NÃO DÃO SUPORTE A ESSA PROPRIEDADE.

Essa propriedade aceita alguns valores:
* **ultra-condensed**: Deixa a fonte mais apertada o possível na horizontal.
```
font-stretch: ultra-condensed;
```
* **extra-condensed**: Deixa a fonte um pouco menos apertada.
```
font-stretch: extra-condensed;
```
* **semi-condensed**: Deixa a fonte quase não apertada na horizontal.
```
font-stretch: semi-condensed;
```
* **normal(padrão)**: Esse é o valor padrão. Não deixa a fonte nem apertada nem esticada.
```
font-stretch: normal;
```
* **semi-expanded**: Deixa a fonte quase não esticada.
```
font-stretch: semi-expanded;
```
* **expanded**: Deixa a fonte um pouco mais esticada.
```
font-stretch: expanded;
```
* **extra-expanded**: Deixa a fonte um bem sticada.
```
font-stretch: extra-expanded;
```
* **ultra-expanded**: Deixa a fonte um muito esticada mesmo!
```
font-stretch: ultra-expanded;
```
***

### Customizando a altura da linha com Line-Height

Agora, vamos ver a propriedade **line-height**. Essa propriedade nos permite definir qual será o espaçamento que haverá acima e abaixo de cada linha do nosso texto.

Essa propriedade aceita alguns valores como padrão.

* **normal(padrão)**: Esse é o valor padrão da propriedade. A maioria dos navegadores aplicará a medida **1.2** quando você usa esse valor. Isso depende também da fonte que usarmos.
```
line-height: normal;
```

Podemos passar valores numéricos também:
```
line-height: 2;
```

Mas... O que é esse número que passamos? Basicamente, o **line-height** multiplica o tamanho da sua fonte pelo o valor que você passa dentro dele. Então se você passar o valor 2 para o line-height e a sua fonte for de 16px, o cálculo será: 2 * 16 = 32px.

Note que estamos aumenta a **fonte** e **não necessariamente as letras**. Quando aumentamos a fonte, isso faz com que os espaçamentos em cima e embaixo de cada letra aumentem.

Se usarmos porcentagem, o mesmo acontecerá:
```
font-size: 14px
line-height: 10%;
```
14 * 0,1 = 1,4px. Isso fará com que a altura da linha caia drasticamente. 

A recomendação é que usemos uma altura de linha de **1.2** no mínimo.   
***

### Propriedade Resumida Font

Assim como em outras seções a propriedade **font** é um **shorthand** para outras propriedades. Se formos usá-la, precisamos passar os valores na seguinte ordem:

* font-style;
* font-variant;
* font-weight;
* font-size/line-height;
* font-family;

Exemplo:

```
font: italic small-caps bold 24px/2 Arial, serif;
```
***


