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

## 9 Nem tudo é o que parece

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
float: right;
```
Para impedir que um elemento tenha um float na sua linha:

```css
clear: right;
```

>Todos os elementos flutuantes ficam em uma linha

>Corrigir o posicionamento dos elementos não flutuantes é chamado de *clearfix*