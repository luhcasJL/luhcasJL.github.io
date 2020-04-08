---
layout: post
title:  "Estrutura com html semântico"
date:   2019-05-02 11:39:00 -0200
categories: templates
permalink: /:categories/:title.html
author: "Lucas"
description: "Semântica, refatorando código anterior"
---

Boas devs,

O artigo anterior [Estrutura com div](http://lucasalves.ml/templates/estrutura-com-div.html), tinha como objetivo ensinar a utilização da div para dividir elementos da página; Eu não me preocupei muito com a parte semântica do HTML5 por que não era o objetivo do artigo e fui aplaudido por alguns (tanto novatos como experientes que entenderam o objetivo do artigo) e também tomei umas voadoras de pessoas que acham que sabem muito e estão a anos luz na frente de todo mundo.

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/w3c.png" style="height: 200px; "/>
</div>

Dito isto peço perdão por não ter feito um código semântico no artigo anterior e vamos refatorar o código anterior.

<h4 style="color: red;">Refatorar</h4>

<blockquote style="color: #000;">Refatoração (do inglês Refactoring) é o processo de modificar um sistema de software para melhorar a estrutura interna do código sem alterar seu comportamento externo. (Wikipédia)</blockquote>

A estrutura em questão era esta:

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/um.png"/>
</div>

Deixo aqui o código html anterior.

{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <div class="conteudo">
      <div class="cabecalho">cabecalho</div>
      <div class="banner">banner</div>
      <div class="areas">
        <div class="area_esquerda">esquerda</div>
        <div class="area_central">central</div>
        <div class="area_direita">direita</div>
      </div>
      <div class="rodape">rodape</div>
    </div>
  </body>
</html>
{% endhighlight %}

Eu não vou mudar o nome das classes para não precisar alterar o css.

Separa a parte que mais interessa neste momento

{% highlight html %}
<body>
  <div class="conteudo">
    <div class="cabecalho">cabecalho</div>
    <div class="banner">banner</div>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
    <div class="rodape">rodape</div>
  </div>
</body>
{% endhighlight %}

Primeiramente eu vou passar a classe conteúdo para a body devido o funcionamento dela.

{% highlight html %}
<body class="conteudo">
  <div>
    <div class="cabecalho">cabecalho</div>
    <div class="banner">banner</div>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
    <div class="rodape">rodape</div>
  </div>
</body>
{% endhighlight %}

Em seguida a div cabeçalho vou colocar pro lado de fora da div anterior e mudar para header.

O header é utilizado para declarar o cabeçalho de um documento ou seção.

{% highlight html %}
<body class="conteudo">
  <header class="cabecalho">cabecalho</header>
  <div>
    <div class="banner">banner</div>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
    <div class="rodape">rodape</div>
  </div>
</body>
{% endhighlight %}

A próxima coisa a fazer é mudar a próxima div para main. A main é onde está o conteúdo principal da página.

{% highlight html %}
<body class="conteudo">
  <header class="cabecalho">cabecalho</header>
  <main>
    <div class="banner">banner</div>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
    <div class="rodape">rodape</div>
  </main>
</body>
{% endhighlight %}

Sendo assim, a div rodapé deverá ficar fora da main, e mudaremos para o nome footer.

{% highlight html %}
<body class="conteudo">
  <header class="cabecalho">cabecalho</header>
  <main>
    <div class="banner">banner</div>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
  </main>
  <footer class="rodape">rodape</footer>
</body>
{% endhighlight %}

A div banner pode ser colocada fora da main também, mudaremos esta div para section. A tag section define seções em um documento.

{% highlight html %}
<body class="conteudo">
  <header class="cabecalho">cabecalho</header>
  <section class="banner">banner</section>
  <main>
    <div class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </div>
  </main>
  <footer class="rodape">rodape</footer>
</body>
{% endhighlight %}

Mudaremos a div areas para section também.

{% highlight html %}
<body class="conteudo">
  <header class="cabecalho">cabecalho</header>
  <section class="banner">banner</section>
  <main>
    <section class="areas">
      <div class="area_esquerda">esquerda</div>
      <div class="area_central">central</div>
      <div class="area_direita">direita</div>
    </section>
  </main>
  <footer class="rodape">rodape</footer>
</body>
{% endhighlight %}

As divs de dentro da section areas, podem ser seções ou apenas div, vai depender do uso, se elas forem seções a conterem artigos elas devem ser seções, se foram divisões para planos por exemplo, podem ser divs. Veja imagem abaixo.

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/planos.PNG"/>
</div>


Considerações finais,

A parte semântica é muito importante sim em um código, ajuda os buscadores a encontrar e entender melhor o contexto, além de facilitar a manutenção futura.

Todavia, existem milhões de sites legados ao sol, se você for o tipo de desenvolvedor nutela que torce o nariz toda vez que vê algo que não está atual, sinto muito, você é um trouxa.

Todos os leitores são bem vindos, embora o blog seja focado a desenvolvedores menos experientes.

Aos novos desenvolvedores, não desanimem, o caminho é árduo mas no final vale a pena, não se esqueçam que entre o "#000000;" e o "#FFFFFF;" existem milhões de cores; e algumas dezenas de tecnologias.

Espero que tenham gostado, é sempre feito com bastante afinco e carinho.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/templates/estrutura-com-div.html">Estrutura com div</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/bate-papo/corrida-pelo-conhecimento.html">Corrida pelo conhecimento</a></div>

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
