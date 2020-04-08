---
layout: post
title:  "CSS - Parte 4 - Conceitos básicos"
date:   2019-04-01 15:29:53 -0200
categories: front-end/css
permalink: /:categories/:title.html
author: "Lucas"
description: "Text (color, text-align, text-decoration, text-transform, text-indent, letter-spacing, line-height, word-spacing), Fonts (font-family, font-size, font-weight, font-style, Fonte Responsiva)"
---

Boas devs, hoje mais um artigo de css.

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/css.jpeg"/>
</div>
<br>
Neste artigo veremos:

- Text
- Fonts

Lembre-se de criar os arquivos e testar os códigos para entender melhor o funcionamento.

<h4 style="color: red;">Text</h4>

Os textos são partes fundamentais de qualquer site, sendo assim eles também devem ser estilizados para a melhor compreensão do conteúdo. Algumas formas de estilizar são:

- color
- text-align
- text-decoration
- text-transform
- text-indent
- letter-spacing
- line-height
- word-spacing

<h4 style="color: red;">Color</h4>

Podemos dar cor a um texto de 3 formas.

<strong>Cor do nome</strong>
{% highlight css %}
p{
  color: red;
}
{% endhighlight %}

<strong>Hexadecimal</strong>

Os 2 primeiros dígitos correspondem ao "Red", os dois seguintes ao "Green" e os dois últimos ao "Blue".
A formação vai de 0 a F. Sendo o 00 nada de cor e o FF o máximo de cor. Na combinação abaixo teremos o vermelho, usando o máximo de vermelho e nada de verde e azul.

{% highlight css %}
p{
  color: #FF0000;
}
{% endhighlight %}

São 16 milhões de combinações possíveis. Tem diversos sites na internet com as cores e os respectivos códigos. Considere estudar teoria das cores (costuma ser serviço do designer) para melhores layouts.

<strong>RGB</strong>

O funcionamento é similar ao HEX, com diferença que vai de 0 a 255.

{% highlight css %}
p{
  color: rgb(255,0,0);
}
{% endhighlight %}

<strong>RGBA</strong>

O funcionamento é similar ao RGB, e tem inclusão de um novo atributo chamado "alpha".
O "alpha" cuida da opacidade (mais claro ou mais escuro), vai de 0 a 1.

{% highlight css %}
p{
  color: rgb(255,0,0,0.2);
}
h1{
  color: rgb(255,0,255,0.6);
}
{% endhighlight %}

<h4 style="color: red;">text-align</h4>

Define o alinhamento do texto, que podem ser:

<strong>alinhado a esquerda "left"</strong>

{% highlight css %}
p{
  text-aling: left;
}
{% endhighlight %}

<strong>centralizado "center"</strong>

{% highlight css %}
p{
  text-aling: center;
}
{% endhighlight %}

<strong>alinhado a direita "right"</strong>

{% highlight css %}
p{
  text-aling: right;
}
{% endhighlight %}

<strong>justificado "justify"</strong>

{% highlight css %}
p{
  text-aling: justify;
}
{% endhighlight %}

<h4 style="color: red;">text-decoration</h4>

O "text-decoration" coloca ou retira linhas.

<strong>text-decoration: none</strong>

Muito utilizado na tag "a" para retirar o sublinhado

{% highlight css %}
a{
  text-decoration: none;
}
{% endhighlight %}

<strong>text-decoration: overline</strong>

Sublina acima do texto

{% highlight css %}
a{
  text-decoration: overline;
}
{% endhighlight %}

<strong>text-decoration: line-through</strong>

Passa uma linha no meio do texto, risca ele

{% highlight css %}
a{
  text-decoration: line-through;
}
{% endhighlight %}

<strong>text-decoration: underline</strong>

Faz o sublinhado comum

{% highlight css %}
a{
  text-decoration: underline;
}
{% endhighlight %}

<h4 style="color: red;">text-transform</h4>

Transforma o texto em letras maiúsculas ou minúsculas

<strong>uppercase</strong>

Todas as letras em maiúsculo

{% highlight css %}
p{
  text-transform: uppercase;
}
{% endhighlight %}

<strong>lowercase</strong>

Todas as letras em minúsculo

{% highlight css %}
p{
  text-transform: lowercase;
}
{% endhighlight %}

<strong>capitalize</strong>

A primeira letra de cada palavra em maiúsculo

{% highlight css %}
p{
  text-transform: capitalize;
}
{% endhighlight %}

<h4 style="color: red;">text-indent</h4>

Define um espaço a primeira linha do paragrafo

{% highlight css %}
p{
  text-indent: 2%;
}
{% endhighlight %}

<h4 style="color: red;">letter-spacing</h4>

Define o espaço entre as letras de um texto

{% highlight css %}
p{
  letter-spacing: 0.1%;
}
{% endhighlight %}

<h4 style="color: red;">line-height</h4>

Define a distância entre uma linha e outra.

{% highlight css %}
p{
  line-height: 1.2;
}
{% endhighlight %}

<h4 style="color: red;">word-spacing</h4>

Define a distância entre uma palavra e outra.

{% highlight css %}
p{
  word-spacing: 0.1%;
}
{% endhighlight %}

<h4 style="color: red;">Fonts</h4>

A tag "font" define o tipo da letra, o tamanho, a largura entre outras coisas.

<h4 style="color: red;">font-family</h4>

Um ótimo local para encontrar tipos variados de fontes é o [google fonts](https://fonts.google.com/).
Você vai lá, escolhe as fontes que você quer usar copia o link passados das fontes implementa da seguinte forma.

Cola o link dentro do "head"
{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
    <link href="https://fonts.googleapis.com/css?family=Indie+Flower|ZCOOL+XiaoWei" rel="stylesheet">
  </head>
  <body>

  </body>
</html>
{% endhighlight %}

Chama a fonte pelo "font-family"
{% highlight css %}
p{
  font-family: 'ZCOOL XiaoWei', serif;
}
h1{
  font-family: 'Indie Flower', cursive;
}
{% endhighlight %}

<h4 style="color: red;">font-size</h4>

Define o tamanho da fonte.

{% highlight css %}
p{
  font-size: 1rem;
}
{% endhighlight %}

Ver [unidades de medidas](http://lucasalves.ml/front-end/css/css-parte-dois-conceitos-basicos.html)

<h4 style="color: red;">font-weight</h4>

Define a largura da letra.

{% highlight css %}
p{
  font-weight: bold;
}
{% endhighlight %}

Alguns possíveis são: "normal", "bold", "bolder", "lighter", "100", "200" a "900".

<h4 style="color: red;">font-style</h4>

Dá pra colocar em itálico

{% highlight css %}
p{
  font-style: italic;
}
{% endhighlight %}

<h4 style="color: red;">Fonte Responsiva</h4>

E o mais legal que aprendi recentemente (felizmente nessa área você nunca para de aprender coisas novas).

Nesse o tamanho da fonte acompanha o tamanho da tela.

{% highlight css %}
p{
  font-size: 8vw;
}
{% endhighlight %}


Por hoje é só, tem bastante coisa legal sobre textos e fontes a serem aprendidas a cada dia que você usa, espero que tenham gostado.

Encontrou algum erro de português? Deixe nos comentários, será bastante útil.

<br>
<hr>
<br>

<div style="width: 30%; float: left;">
  <img src="/assets/imagens/foto.jpg" style="height: 150px; width: 150px; border-radius: 50%;"/>
</div>

<div style="width: 100%;">
  <h3>Lucas Alves</h3>
  <h4>Desenvolvedor Full Stack - Desde 2017</h4>
</div>

<br><br><br>
<hr>
<br>

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/front-end/html/html-parte-quatro-conceitos-basicos.html">HTML - Parte 4 - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/bate-papo/habilidades-a-serem-aprendidas.html">Habilidades a serem aprendidas</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte 5 - Conceitos básicos
- Lógica de Programação - Parte I
- JavaScript - Parte I
- CPanel - Guia definitivo
- Resenha: Livro A Lei de Murphy no Gerenciamento de projetos

<br><br>
Comentem aqui em baixo, marquem gostei, tirem dúvidas, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>

{% include disqus.html %}
