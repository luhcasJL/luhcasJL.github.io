---
layout: "post"
title: "Primeiro layout"
date:   2019-03-13 16:29:53 -0200
categories: templates
permalink: /:categories/:title.html
description: "Fazendo um layout do zero com base em um site pronto"
---

Para o primeiro layout que eu apresento aqui neste blog, pegarei como exemplo o template gratuito [Primex](https://www.templatemonster.com/pt-br/demo/51695.html) do site [templatemonster](https://www.templatemonster.com/pt-br/) .

<img src="/assets/imagens/primex/layout.png" />

Para este projeto não usarei o CodeIgniter, farei a estrutura conforme abaixo.

<img src="/assets/imagens/primex/estrutura.JPG" style="float: left; margin-right: 5%;"/>

Explicando a estrutura:

- Primeiro eu criei a pasta chama primex e coloquei dentro dela as pastas assets e elements, e também coloquei o arquivo index.php

- A pasta assets eu uso para colocar tudo referente a CSS, JS e imagens.
  Coloquei na pasta css o arquivo do bootstrap e um arquivo vazio chamado style.css
  Na pasta js coloquei o jquery, o bootstrap e o tether.

- A pasta elements eu coloco os arquivos que sempre se repetirão no site.
  O arquivo header serve principalmente para colocar o '<head>', os '<meta>' e chamar os arquivos CSS.
  O arquivo sidebar eu uso para fazer a barra de navegação do site.
  E o arquivo footer serve principalmente para colocar o rodapé e chamar os arquivos JS.

<div style="clear: both;"></div>

<br>
Tudo pronto, mãos ao código.

Começo colocando os seguintes códigos nos

header.php
{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Primex</title>

    <meta name="description" content="Aqui vem a descrição do site">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <link href="assets/css/bootstrap.css" rel="stylesheet">
    <link href="assets/css/style.css" rel="stylesheet">
  </head>
  <body>
{% endhighlight %}

footer.php
{% highlight html %}
  </body>
</html>
<script src="assets/js/jquery-3.1.0.js"></script>
<script src="assets/js/tether.js"></script>
<script src="assets/js/bootstrap.js"></script>
{% endhighlight %}

e chamo os elements no

index.php
{% highlight php %}
<?php include('elements/header.php'); ?>
<?php include('elements/sidebar.php'); ?>

<?php include('elements/footer.php'); ?>
{% endhighlight %}

Se abrirmos o index.php no navegador não veremos nada além de uma tela branca, contudo agora podemos iniciar o front-end de fato. A começar pela barra de navegação.

E voa-la

<img src="/assets/imagens/primex/navbar.JPG" />

Agora vamos ao código

sidebar.php

{% highlight  php %}
<?php $paginaCorrente = basename($?>
<header>
<!-- Barra de navegação -->
<nav class="navbar navbar-fixed-top navbar-light bg-light container navheader">
  <img src="assets/img/logo.png" alt="logotipo Primex" id="logotipo" class="navbar-brand">
  <button class="navbar-toggler hidden-md-up float-sm-right float-xs-right" type="button" data-toggle="collapse" data-target="#menu-sanduiche"></button>
  <div class="collapse navbar-toggleable-sm" id="menu-sanduiche">
    <ul class="nav navbar-nav float-md-right">
      <li  <?php if($paginaCorrente != 'about' && $paginaCorrente != 'services' && $paginaCorrente != 'blog' && $paginaCorrente != 'contact') {echo 'class="nav-item corrente"';}else{echo 'class="nav-item"';} ?>>
        <br class="hidden-sm-up">
        <a href="home" class="nav-link">Home</a>
      </li>
      <li class="nav-item" <?php if($paginaCorrente == 'about') {echo 'class="nav-item"';}else{echo 'class="nav-item"';} ?>>
        <a href="about" class="nav-link">About</a>
      </li>
      <li class="nav-item" <?php if($paginaCorrente == 'services') {echo 'class="nav-item"';}else{echo 'class="nav-item"';} ?>>
        <a href="services" class="nav-link">Services</a>
      </li>
      <li class="nav-item" <?php if($paginaCorrente == 'blog') {echo 'class="nav-item"';}else{echo 'class="nav-item"';} ?>>
        <a href="blog" class="nav-link">Blog</a>
      </li>
      <li class="nav-item" <?php if($paginaCorrente == 'contact') {echo 'class="nav-item"';}else{echo 'class="nav-item"';} ?>>
        <a href="contact" class="nav-link">Contacts</a>
      </li>
    </ul>
  </div>
</nav>
<!-- Fim - Barra de navegação -->
</header>
{% endhighlight %}

Essa estrutura HTML eu peguei quase pronta na documentação do Bootstrap, você pode encontrar diversos modelos no link https://getbootstrap.com/docs/4.0/components/navbar/ e fiz algumas adaptações, define que ela ficaria dentro do "container" e também criei uma classe de nome "navheader" e também defini que a lista flutuaria a direita com "float-md-right". Eu também coloquei um php no inicio da página que pega o último valor da url e assim eu sei qual link deverá ser estilizado.

A partir dai foi tudo no css.

style.css
{% highlight css %}
body{
  margin-top: 0;
  padding-top: 0;
}

.navheader{
  height: 66px;
  position: absolute;
}

#logotipo{
  height: 66px !important;
  width: auto;
}

.navbar-nav{
  width: 55%;
}

.nav-item{
  position: relative;
  top: -8px;
  margin-left: 5%;
  margin-right: 5%;
  padding: 20px 10px 10px 10px;
  height: 66px;
}

.nav-item:hover, .corrente{
  color: #02918D;
  background-color: #edecec;
  border-bottom: 4px solid #02918D;
}
{% endhighlight %}

Eu estou levando em consideração que o leitor conheça estes atributos do css, caso não conheça acesse [este link](https://www.w3schools.com/css/).

O próximo item que temos nessa página é o carrousel, [clique aqui](https://getbootstrap.com/docs/4.0/components/carousel/) e veja a documentação no bootstrap.

<img src="/assets/imagens/primex/banner.JPG" />

Essas setas são ícones do font-awesome, então eu precisei importar primeiro o css deles na página header.php

{% highlight html %}
link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css" integrity="sha384-fnmOCqbTlWIlj8LyTjo7mOUStjsKC4pOpQbqyi7RrhN7udi9RwhKkMHpvLbHG9Sr" crossorigin="anonymous">
{% endhighlight %}

Eu comecei criando uma section chamada banner e colando um [carousel](https://getbootstrap.com/docs/4.0/components/carousel/) do bootstrap.

{% highlight html %}
<?php include('elements/header.php'); ?>
<?php include('elements/sidebar.php'); ?>
<section id="banner">
  <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100 img_banner" src="assets/img/banner_1.JPG" alt="First slide">
      <div class="conteudo_banner">
        Solutions that you need!
      </div>
      <div class="campo_more_info">
        <button type="button" name="button" class="btn more_info">More info</button>
      </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100 img_banner" src="assets/img/banner_2.JPG" alt="Second slide">
      <div class="conteudo_banner">
        Lorem ipsum dolor sit!
      </div>
      <div class="campo_more_info">
        <button type="button" name="button" class="btn more_info">More info</button>
      </div>
    </div>
    <div class="carousel-item">
      <img class="d-block w-100 img_banner" src="assets/img/banner_3.Jpg" alt="Third slide">
      <div class="conteudo_banner">
        Lorem ipsum dolor sit!
      </div>
      <div class="campo_more_info">
        <button type="button" name="button" class="btn more_info">More info</button>
      </div>
    </div>
  </div>
  <a class="carousel-control-prev " href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"><i class="fas fa-angle-left fa-4x float-md-left float-sm-left float-xs-left botao_esquerdo"></i></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span class="carousel-control-next-icon " aria-hidden="true"><i class="fas fa-angle-right fa-4x float-md-right float-sm-right float-xs-right botao_direito"></i></span>
    <span class="sr-only">Next</span>
  </a>
</div>
</section>
<?php include('elements/footer.php'); ?>
{% endhighlight %}

Eu fiz algumas adaptações e criei algumas classe que usei no style.css

{% highlight css %}
#banner{
  // serve para que o banner não ocupe o espaço / fique atrás da barra de navegação
  position: relative;
  top: 66px;
}

.botao_esquerdo, .botao_direito{
  color: #232222;
  background-color: #d4d8d8;
  height: 80px;
  width: 80px;
  border: 1px solid #d4d8d8;
  border-radius: 50%;
  position: relative;
  top: -410px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.botao_esquerdo{
  left: 5%;
}

.botao_direito{
  right: 5%;
}

.img_banner{
  filter: contrast(70%);
  filter: brightness(60%);
}

.conteudo_banner{
  text-align: center;
  position: relative;
  top: -330px;
  color: #fff;
  font-size: 4rem;
  font-weight: 100;
}

.campo_more_info{
  text-align: center;
  position: relative;
  top: -200px;
}

.more_info{
  height: 60px;
  font-weight: lighter;
  font-family: 'Marvel',sans-serif;
  font-size: 1.5rem;
  padding: 15px 51px 16px;
  background-color: #f1f045 !important;
  border-radius: 0 !important;
}
{% endhighlight %}

Uma coisa importante que quero que percebam é que vamos fazendo pedaço por pedaço sem preocupar com o restante do site, muitas vezes queremos fazer tudo de uma vez e acabamos não fazendo nada.

Nota: Estou usando o modelo apenas como exemplo, então não estou fazendo com toda a fidelidade como seria em um trabalho profissional.

Vamos a próxima parte do layout.

<img src="/assets/imagens/primex/servicos.JPG" />

Nessa parte a maior parte do trabalho foi pegar alguns icones do [fontawesome](https://fontawesome.com/icons?d=gallery) e estilizar no css.

{% highlight html %}
<section id="servicos" class="container">
  <div class="row">
    <div class="col-md-3 caixa">
      <i class="fas fa-percent fa-2x icone"></i>
      <br>
      <a href="#"><h4>Budget Planning</h4></a>
      <p>Lorem ipsum dolor sit amettetur dipiscing elit. In mollis erat mattis</p>
      <br>
      <button type="button" name="button" class="btn btn_read_more">read more</button>
    </div>
    <div class="col-md-3 caixa">
      <i class="fas fa-signal fa-2x icone"></i>
      <br>
      <a href="#"><h4>Marketing Research</h4></a>
      <p>Lorem ipsum dolor sit amettetur dipiscing elit. In mollis erat mattis</p>
      <br>
      <button type="button" name="button" class="btn btn_read_more">read more</button>
    </div>
    <div class="col-md-3 caixa">
      <i class="fas fa-user-alt fa-2x icone"></i>
      <br>
      <a href="#"><h4>Employee Benefits</h4></a>
      <p>Lorem ipsum dolor sit amettetur dipiscing elit. In mollis erat mattis</p>
      <br>
      <button type="button" name="button" class="btn btn_read_more">read more</button>
    </div>
    <div class="col-md-3 caixa">
      <i class="fas fa-wrench fa-2x icone"></i>
      <br>
      <a href="#"><h4>Risk Management</h4></a>
      <p>Lorem ipsum dolor sit amettetur dipiscing elit. In mollis erat mattis</p>
      <br>
      <button type="button" name="button" class="btn btn_read_more">read more</button>
    </div>
  </div>
  <br><br>
</section>
{% endhighlight %}

Note que eu utilizei "col-md-3 col-sm-6 col-xs-12", estas classes servem para deixar o layout responsivo, o "col-md-3" diz que nas telas medias (notebook e computadores) ele deve utilizar 3 colunas da página, o "col-sm-6" diz que nas telas pequenas (tablets e celulares deitados) deve ser utilizados 6 colunas e na "col-xs-12" que nas telas pequenas (celulares em geral) deverá usar as 12 colunas da tela.

{% highlight css %}
.icone{
  color: #02918D;
  height: 100px;
  width: 100px;
  border: 2px solid #02918D;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.btn_read_more{
  background-color: #f1f045 !important;
  border-radius: 0 !important;
}
{% endhighlight %}

Um trecho de código css impressionante e que já utilizei pela segunda vez nestre projeto foi

{% highlight css %}
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
{% endhighlight %}

Ele é responsável por alinhar um item no centro em todas as direções, nos casos em que usei foi pra centralizar os ícones na borda circular.

<img src="/assets/imagens/primex/info.JPG" />

Segue código

{% highlight html %}
<section id='info' class="container">
  <h2>The Best Marketing Services,</h2>
  <h2>Data & Analysis</h2>
  <br>
  <p>
    Visit our official blog for more detailed information about this freebie. <br>
    Want more business themes ? Check out the same name category at TemplateMonster.com.
  </p>
  <p>
    Vivamus at magna non nunc tristique rhoncus. Aliquam nibh ante, egestas id dictum a, commodo luctus libero. Praesent faucibus malesuada faucibus. Donec laoreet metus id laoreet malesuada. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam consectetur orci sed
  </p>
</section>
{% endhighlight %}

{% highlight css %}
#info{
  margin-top: 80px;
  text-align: center;
}

#info h2{
  color: #129894;
}
{% endhighlight %}

Para o artigo não ficar muito extenso e para não entregar a obra da [templatemonster](https://www.templatemonster.com/pt-br/) vamos parar por aqui. [GitHub](https://github.com/luhcasJL/blog/tree/master/primex) do código.

Comentem aqui em baixo, tirem dúvidas, de sugestão, e esperem pelo novo artigo.

Tem um layout curioso? Mande para mim e tentaremos desvenda-lo.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.

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


<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/jekyll/objetivos-do-blog.html">Objetivos do blog</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/conceitos/mvc-uma-breve-explicacao.html">MVC - Uma breve explicação</a></div>

<br><br>
{% include disqus.html %}
