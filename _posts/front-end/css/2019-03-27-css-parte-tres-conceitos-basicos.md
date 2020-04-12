---
layout: post
title:  "CSS - Parte 3 - Conceitos básicos"
date:   2019-03-27 14:57:53 -0200
categories: front-end/css
permalink: /:categories/:title.html
author: "Lucas"
description: "Border, Margin, Padding"
---

Boas devs, no artigo de hoje vamos aprofundar mais nas tags vistas no primeiro [artigo](https://programadoresreais.com.br/front-end/css/css-parte-um-conceitos-basicos.html) de css.

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/css.jpeg"/>
</div>
<br>
Neste artigo veremos:

- Border
- Margin
- Padding

Depois de termos visto sobre [Unidades de Medidas](https://programadoresreais.com.br/front-end/css/css-parte-dois-conceitos-basicos.html), fica mais fácil de entender esses conceitos.

Para entender este novo artigo, crie a pasta "aula_tres", o arquivo "index.html" e o "style.css".

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
    <div class="um"></div>
    <div class="dois"></div>
    <div class="tres"></div>
    <div class="quatro"></div>
  </body>
</html>
{% endhighlight %}

style.css
{% highlight css %}
div{
  height: 50px;
  width: 50px;
}
{% endhighlight %}

<h4 style="color: red;">Border</h4>

Naquele primeiro artigo vimos a utilização desta forma

{% highlight css %}
div{
  border: 1px solid #FF0000;
}
{% endhighlight %}

Este modo é bem correto, ele define borda de 1px em todos os lados, do tipo solido, e da cor vermelha. Mas e se quisermos fazer só do lado esquerdo?

{% highlight css %}
.um{
  border-left: 2px solid #FF0000;
}
{% endhighlight %}

Assim sendo temos as seguintes propriedades.

{% highlight css %}
.um{
  border-top: 2px solid #FF0000;
  border-right: 2px solid #FF0000;
  border-bottom: 2px solid #FF0000;
  border-left: 2px solid #FF0000;
}
{% endhighlight %}

Desta forma, podemos definir expessuras, tipos e cores diferentes para cada borda.

Tipos de bordas:

- dotted
- dashed
- solid
- double
- groove
- ridge
- inset
- outset
- none
- hidden

A melhor forma de conhece-las é testando uma a uma.

{% highlight css %}
.um{
  border-top: 2px groove #FF0000;
  border-right: 2px dotted #FF0000;
  border-bottom: 2px dashed #FF0000;
  border-left: 2px ridge #FF0000;
}
{% endhighlight %}

Também podemos declarar propriedade por propriedade.

{% highlight css %}
.dois{
  border: 2px;
  border-color: #0000FF;
  border-style: solid;
}
{% endhighlight %}

<h4 style="color: red;">Margin</h4>

Usamos para definir o espaço a ser respeitado pelos outros elementos. Declaramos no primeiro artigo desta forma:

{% highlight css %}
div{
  margin: 1%;
}
{% endhighlight %}

Deste modo definimos que ele deve se afastar em 1% em todas as direções. Outro modo válido é:

{% highlight css %}
.um{
  margin-top: 1%;
  margin-right: 1%;
  margin-bottom: 1%;
  margin-left: 1%;
}
{% endhighlight %}

E o modo mais interessante:

{% highlight css %}
.dois{
  margin: 5px 1% 5% 0;
}
{% endhighlight %}

Definimos em uma única propriedade, o primeiro é o top (topo), o segundo o right (esquerdo), o terceiro o bottom (inferior) e o quarto o left.

Podemos declarar unidades de medidas diferentes, e se quisermos que seja zerado, se coloca o 0 (zero) sozinho, se colocar 0px ele pode acabar definindo um valor em porcentagem herdado de outro valor.

<h4 style="color: red;">Padding</h4>

Aqui são as mesmas explicações do margin com a única diferença que é o espaço interno, como explicado no primeiro artigo.

Esse foi um artigo bem rápido para explicar outras formas de implementar estas propriedades.

Continue acompanhando o blog, é feito de coração para ensinar o máximo de coisas possíveis, assine a notificação pra ficar por dentro de tudo.

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/front-end/html/html-parte-tres-conceitos-basicos.html">HTML - Parte 3 - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/front-end/html/html-parte-quatro-conceitos-basicos.html">HTML - Parte 4 - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- HTML - Parte 4 - Conceitos básicos
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
