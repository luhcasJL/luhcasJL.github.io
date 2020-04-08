---
layout: post
title:  "HTML - Parte 2 - Conceitos básicos"
date:   2019-03-21 14:30:53 -0200
categories: front-end/html
permalink: /:categories/:title.html
author: "Lucas"
description: "Comentários, Imagens, Formatos de texto, Citações"
---

Boas devs, essa é a parte 2 da série HTML - Conceitos Básicos e continuação da série que pretende tornar-te desenvolvedor Full Staaaaack.

<div style="text-align: center;">
  <img src="/assets/imagens/html/html.png"/>
</div>

No artigo [anterior](http://lucasalves.ml/front-end/html/html-parte-um-conceitos-basicos.html) aprendemos alguns conceitos iniciais e algumas tags:

Neste artigo veremos:

- Comentários
- imagens
- Formatos de texto
- Citações

Na sua pasta do html, salve uma nova pasta chamada aula_dois e crie o "index.html" e faça a estrutura padrão do html.

{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Aula dois</title>
  </head>
  <body>

  </body>
</html>
{% endhighlight %}

Salve e abra o arquivo no navegador, lembre-se de salvar e atualizar o navegador todas as vezes para ver o que está acontecendo.

Obs.: Os códigos ficam dentro do body.

<h4 style="color: red;">Comentários</h4>

Os comentários servem para deixar alguma informação para os analistas futuros que virão a fazer manutenção no código, no html eles são feitos assim:

Comentário de 1 linha
{% highlight html %}
<!-- Este é um comentário -->
{% endhighlight %}

Comentário de várias linhas
{% highlight html %}
<!--
<p>Eu sou um paragrafo.</p>
-->
{% endhighlight %}

O HTML que estiver dentro do comentário será ignorado pelo navegador e não será mostrado.

<h4 style="color: red;">Imagens</h4>

Uma imagem é colocada no html da seguinte forma.

{% highlight html %}
<img src="http://www.fundosanimais.com/1920x1080/imagens-tigres.jpg" alt="Tigre branco" width="104" height="142">
{% endhighlight %}

A tag img recebe o atributo src="" que é o caminho onde está a imagem, o atributo atl="" que é um texto a ser apresentado caso a imagem não possa carregada e dois atributos opcionais que são o width para largura e height para altura da imagem, recomenda-se usar o css para definir estes atributos.

Outra forma de chamar uma imagem é tê-la salva no projeto.

{% highlight html %}
<!-- se estiver na mesma pasta que o arquivo html -->
<img src="tigre.jpg" alt="Tigre branco" width="104" height="142">

<!-- se estiver em uma pasta diferente do arquivo html, você coloca o caminho da imagem -->
<img src="img/animal/tigre.jpg" alt="Tigre branco" width="104" height="142">
{% endhighlight %}

<h4 style="color: red;">Formatos de texto</h4>

Existem algumas tags especiais para formatos de texto, confira abaixo.

<h4 style="color: red;">Texto pré-formatado</h4>
A tag pre mantém os espaços e quebras de linhas e dá uma estilizada no texto.

{% highlight html %}
<p>Eu sou um paragrafo e estou aqui pra você conseguir perceber o pre.</p>
<pre>
No meio do caminho tinha uma pedra

tinha uma pedra no meio do caminho

tinha uma pedra

no meio do caminho tinha uma pedra.
</pre>
{% endhighlight %}

<h4 style="color: red;">Texto em negrito</h4>
2 formas de deixar o texto em negrito.
{% highlight html %}
No meio do <b>caminho</b> tinha uma pedra.
<br>
No meio do <strong>caminho</strong> tinha uma pedra.
{% endhighlight %}

<h4 style="color: red;">Texto em italico</h4>
2 formas de deixar o texto em itálico.
{% highlight html %}
No meio do <i>caminho</i> tinha uma pedra.
<br>
No meio do <em>caminho</em> tinha uma pedra.
{% endhighlight %}

<h4 style="color: red;">Texto small </h4>

{% highlight html %}
<h2>No meio do <small>caminho</small> tinha uma pedra.</h2>
{% endhighlight %}

<h4 style="color: red;">Texto marcado </h4>

{% highlight html %}
<h2>No meio do <mark>caminho</mark> tinha uma pedra.</h2>
{% endhighlight %}

<h4 style="color: red;">Texto deletado</h4>

{% highlight html %}
<p>No meio do <del>caminho</del> tinha uma pedra.</p>
{% endhighlight %}

<h4 style="color: red;">Texto sublinhado </h4>

{% highlight html %}
<p>No meio do <ins>caminho</ins> tinha uma pedra.</p>
{% endhighlight %}

<h4 style="color: red;">Texto abaixo </h4>

{% highlight html %}
<p>No meio do <sub>caminho</sub> tinha uma pedra.</p>
{% endhighlight %}

<h4 style="color: red;">Texto acima </h4>

{% highlight html %}
<p>No meio do <sup>caminho</sup> tinha uma pedra.</p>
{% endhighlight %}

<strong>A melhor forma de ver o que cada um faz e se lembrar depois é testando, poderia tirar print de um por um e colocar aqui? Poderia, vou fazer? Hoje não, tenho outros projetos também "rapaiz".</strong>

<h4 style="color: red;">Citações</h4>

Abaixo as tags de citação.

<h4 style="color: red;">Citação comum</h4>

Nada mais que aspas duplas --'

{% highlight html %}
<p>No meio do <q>caminho</q> tinha uma pedra.</p>
{% endhighlight %}

<h4 style="color: red;">Citação de verdade ^^</h4>

{% highlight html %}
<p>Eu sou um paragrafo e estou aqui pra você conseguir perceber o blockquote.</p>
<blockquote cite="aqui_vai_o_caminho_do_arquivo_original.html">
No meio do caminho tinha uma pedra
tinha uma pedra no meio do caminho
tinha uma pedra
no meio do caminho tinha uma pedra.
</blockquote>
{% endhighlight %}

<h4 style="color: red;">Abreviação com citação</h4>

{% highlight html %}
<p>Eu trabalhei na <abbr title="Força Aérea Brasileira">FAB</abbr> por 5 anos e meio.</p>
{% endhighlight %}

<h4 style="color: red;">Citação de endereço</h4>

{% highlight html %}
<address>
Written by John Doe.<br>
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
{% endhighlight %}

<h4 style="color: red;">Citação de obra</h4>

{% highlight html %}
<p><cite>A Mona Lisa</cite> é uma pintura de Leonardo da Vinci.</p>
{% endhighlight %}

<h4 style="color: red;">Texto ao contrário</h4>

Sabe aquela brincadeira de falar ao contrário? Então.

{% highlight html %}
<p><bdo dir="rtl">Eu não sei lidar com isso.</bdo></p>
{% endhighlight %}

Estes foram alguns exemplos do que foi proposto no inicio do artigo, espero que estejam gostando, logo iremos fazer layouts poderosos.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/front-end/css/css-parte-um-conceitos-basicos.html">CSS - Parte 1 - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/front-end/css/css-parte-dois-conceitos-basicos.html">CSS - Parte 2 - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte II - Conceitos básicos
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
