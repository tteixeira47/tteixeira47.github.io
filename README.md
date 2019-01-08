# tteixeira47.github.io

Repositório para aprendizagem de HTML & CSS.

## 8 - Usando mais seletores

```html
<ul id="social-media">
```

Parâmetro *id* é usado para identificar uma tag.

```css
#social-media li {
  display: inline-block;
}
```

O *#* é usado para identificar um id no CSS.

> Não se deve repetir *id* numa página, por isso deve ser usado em elementos únicos

Por causa disso é usado o parâmetro *class*

```html
<ul class="social-media">
```
O seletor de classe é o ponto (.)

```css
.social-media li {
  display: inline-block;
}
```
É possível usar mais de uma classe no elemento
```html
<ul class="social-media social-media-rodape">
```

## 9 - Nem tudo é o que parece

Para deixar o texto em caixa alte é possível usar o seguinte CSS:

```css
text-transform: uppercase;
```

### Image Replacement

Substituir o texto de um link por uma imagem

```css
.social-media a {
  width: 40px;
  height: 40px;
  display: inline-block;
  text-indent: -9999px;
}
```

### Flutuando elementos

Para que elementos possam flutuar no seu bloco, é utliizado o seguinte CSS:

```css
img {
  float: right;
}
```
Para impedir que um elemento tenha um float na sua linha:

```css
img {
  clear: right;
}
```

>Todos os elementos flutuantes ficam em uma linha

>Corrigir o posicionamento dos elementos não flutuantes é chamado de *clearfix*

## 10 - Elementos onde quisermos

### Posição relativa

Com essa propriedade, o elemento é deslocado em alguns pixels de sua posição original

```css
.foto-joao {
  position: relative;
  top: 50px;
  right: 50px;
}
```

>Relative respeita o fluxo da página

### Posição absoluta

```css
.foto-joao {
  position: absolute;
  top: 50px;
  right: 50px;
}
```

>Absolute não respeita o fluxo da página e é relativo à janela do navegador

### Posição fixa

```css
#rodape {
  position: fixed;
  bottom: 0px;
}
```

>Fixed fixa o elemento em relação à tela

# PARTE 2 - HTML & CSS Avançado

## 1 - Pixels

### Medidas relativas

O tamanho da fonte é definido de acordo com a medida do navegador

>Elementos usam medidas de outros elementos como referência

#### Medida rem

Utiliza o tamanho da fonte do navegador como base

```css
.classe {
  font-size: 1.25rem;
}
```

#### Medida ch

Utiliza a largura do caracter 0 utilizado

```css
.classe {
  font-size: 1.25ch;
}
```

#### Medida em

Utiliza o tamanho da fonte do elemento como base

```css
.classe {
  font-size: 1.25em;
}
```

## 2 - Absolute

Quando queremos tirar um elemento do fluxo e posicioná-lo em qualquer ponto da página

>É preciso definir o position do elemento pai (o mesmo não pode ser static)

## 3 - Border Radius e novidades CSS3

Propriedade criada para arredondar bordas.

Propriedades beta são lidas de forma diferente em diferentes navegadores.

Portanto, é usado um prefixo pra identificar o navegador:

```css
div {
  -webkit-border-radius: 10 10 10 10 / 5 5 5 5;
  -moz-border-radius: 10 10 10 10;
}
```

>Future proof: escrever a funcionalidade sem prefixo também

Site para testar funcionalidades: [CanIUse](https://caniuse.com)

## 4 - Transformações geométricas

*transform* é a propriedade usada para transformar um objeto geométrico

```css
div {
  transform: rotate(30deg) skew(20deg) scale(1.2) translate(10px, 15px);
}
```

```css
div {
  transform-style: preserve-3d;
}
```

## 5 - Sombras e opacidade

```css
text-shadow: 0 0 1em #000;
box-shadow: 0 0 1em #000, inset 0 0 .5em #FFF;

background-color: rgba(0, 0, 0, .3);
opacity: .3;
```
## 6 - Gradiente

```css
background-image: linear-gradient(to bottom right, white, red, black);

background-repeat: no-repeat;
background-size: 80% 5px;
background-position: 50% 50%;

background-image: radial-gradient(yellow, red);
```

## 6 - Seletores avançados

Para selecionar **todos** os elementos depois de outro elemento é usado o *~*

```css
li ~ li {
  margin-top: 2px;
}
```
Para selecionar **o primeiro** os elementos depois de outro elemento é usado o *+*

```css
li + li {
  margin-top: 2px;
}
```

Para selecionar **o filho** de um elemento é usado o >*

```css
div > p {
  margin-top: 2px;
}
```

>Também existem outros seletores como *[$]* que escolhe o que está escrito no final do arquivo e *[^]* que escolhe o início.