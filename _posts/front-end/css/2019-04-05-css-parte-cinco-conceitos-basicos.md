---
layout: post
title:  "CSS - Parte 5 - Conceitos básicos"
date:   2019-04-05 11:03:53 -0200
categories: front-end/css
permalink: /:categories/:title.html
author: "Lucas"
description: "Height, Width, Float, Position"
---

Boas devs, aproximando-se do fim de "CSS - Conceitos Básicos",

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/css.jpeg"/>
</div>
<br>
Neste artigo:

- height
- width
- float
- position

<h4 style="color: red;">Height e Width</h4>

Os "height" e "width" são respectivamente altura e largura, eles são utilizados para dimensionar ou redimensionar elementos. Considere o seguinte código html como exemplo:

index.html
{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <div id="elemento_um" class="elemento">
      <h1>Elemento 1</h1>
    </div>
    <div id="elemento_dois" class="elemento">
      <h1>Elemento 2</h1>
    </div>
  </body>
</html>
{% endhighlight %}

E o seguinte código CSS:

style.css
{% highlight css %}
.elemento{
  height: 30vh;
  width: 50%;
  border: 2px solid #000;
}
{% endhighlight %}

Vamos ficar com a página assim:

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/um.JPG"/>
</div>

O que fizemos foi definir altura como "30vh" para 30% da altura da tela, e largura como "50%" para definir 50% da largura da tela. Também definimos uma borda para conseguirmos ver os elementos.

<h4 style="color: red;">Float</h4>

O atributo "float" faz o elemento flutuar na página para a esquerda ou para a direita.

style.css
{% highlight css %}
#elemento_dois{
  float: right;
}
{% endhighlight %}

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/dois.JPG"/>
</div>

Definimos que o "id='elemento_dois'" flutue para a direita. Podemos usar para flutuar qualquer elemento de uma página, mas estamos com o objetivo inicial de colocar uma "div" ao lado da outra.

O que precisamos perceber primeiro é que elas não cabem uma ao lado da outra na página, conforme figura acima, então mudaremos primeiro o tamanho delas para "49.7%".

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/tres.JPG"/>
</div>

Agora se percebe que elas cabem cada uma em um lado da página, o que devemos fazer a seguir é definir o "elemento_um" como:

style.css
{% highlight css %}
#elemento_um{
  float: left;
}
{% endhighlight %}

E ficaremos com:

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/quatro.JPG"/>
</div>

A explicação disso é que o "elemento_um" estava ocupando toda a linha mesmo que não estive utilizando toda ela, e quando definimos como "float: left;" liberamos o espaço livre para os elementos que estão abaixo.

O mesmo deve ser feito quando colocamos imagens e queremos que o texto ocupe um dos lados livres.

<h4 style="color: red;">Position</h4>

O "position" como o nome sugere, define a posição que o elemento ficará sobre a página. Existem algumas situações:

- static
- relative
- fixed
- absolute
- sticky

<strong>static</strong>
Posição padrão dos elementos.

<strong>relative</strong>
Esse é de certa forma o mais utilizado de todos.

style.css
{% highlight css %}
#elemento_dois{
  position: relative;
  top: 20px;
}
{% endhighlight %}

Quando definimos com "relative", pode mover o elemento para todas as direções, ele se movimento com relação ao elemento mais próximo.

<strong>fixed</strong>

Para perceber o fixed solte bastante texto na página até que tenha o "scroll". Confira o "gif" abaixo.

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/fixed.gif"/>
</div>

Neste exemplo eu adicionei no html:

index.html
{% highlight html %}
<div class="quadrado">
  fixed
</div>
<p>
  Bastante texto aqui dentro.
</p>
{% endhighlight %}

E no css:

style.css
{% highlight css %}
.quadrado{
  position: fixed;
  left: 40%;
  top: 100px;
  height: 50px;
  width: 50px;
  border: 1px solid #000;
  background-color: #c3c3c3;
}
{% endhighlight %}

O que deve ser percebido aqui é que o elemento fica fixo naquele lugar, mesmo que todo o resto mude, é uma boa escolha pra deixar menus presos no top, ou em algum dos campos.

Nota: Eu aprendi a fazer gif pela necessidade de mostrar o funcionamento do fixed. <3

<strong>absolute</strong>

Uma boa escolha para colocar algum elemento alinhado a direita.

style.css
{% highlight css %}
.quadrado{
  position: absolute;
  right: 0;
}
{% endhighlight %}

<strong>sticky</strong>

O "sticky" é muito legal, vou deixar que vejam por si só.

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_cinco/sticky.gif"/>
</div>

Viu que legal, ele está "static" na página e quando se aproxima do topo fica como "fixed".

Inclui no html:

index.html
{% highlight html %}
<div class="barra">
  <h1>Isto é um sticky</h1>
</div>
{% endhighlight %}

E no CSS:

style.css
{% highlight css %}
.barra{
  clear: both;
  position: sticky;
  top: 0;
  width: 100%;
  border: 2px solid #FF0000;
  background-color: #AA0000;
  text-align: center;
}
{% endhighlight %}

Estes são atributos super importantes para se fazer um bom layout, aprenda-os bem, em breve faremos diversos layouts do zero neste blog.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/bate-papo/habilidades-a-serem-aprendidas.html">Habilidades a serem aprendidas</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/templates/estrutura-com-div.html">Estrutura com div</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte 6 - Conceitos básicos
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
