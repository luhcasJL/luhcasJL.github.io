---
layout: post
title:  "CSS - Parte 1 - Conceitos básicos"
date:   2019-03-19 15:12:53 -0200
categories: front-end/css
permalink: /:categories/:title.html
author: "Lucas"
description: "Definição, Implementação, Estrutura básica, Colors, Backgrounds, Border, Margin, Padding"
---

Continuando a série de artigos que tem o intuito de tornar-te um desenvolvedor Full Stack, o artigo anterior foi [HTML - Parte 1 - Conceitos Básicos](https://programadoresreais.com.br/front-end/html/html-parte-um-conceitos-basicos.html).

<img src="/assets/imagens/css/aula_um/css.jpeg"/>

<h3 style="color: blue; text-align: center;">CSS - Definição</h3>

Cascading Style Sheets (CSS) ou Folha de estilo em cascatas lançada em 1996 para estilizar elementos da página HTML, de forma que não existe websites sem alguma das duas tecnologias.

<h3 style="color: blue; text-align: center;">Implementação</h3>

Existem 3 formas de se implementar o CSS.

<h4 style="color: red;">Inline</h4>

{% highlight html %}
<p style="color: blue;">Eu sou um paragrafo</p>
{% endhighlight %}

* Não aconselhável, css só valerá para o elemento e dificultará muito a manutenção, imagine ter que trocar a cor de 300 parágrafos.

<h4 style="color: red;">Interno</h4>

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>Título da página</title>
    <style>
      p{
        color: blue;
      }
    </style>
  </head>
  <body>
    <p>Eu sou um paragrafo</p>
  </body>
</html>
{% endhighlight %}

* Parcialmente não aconselhável, css só valerá para a página que ele está, desse modo terá que fazer 1 CSS para cada página.

<h4 style="color: red;">Externo</h4>

index.html
{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>Título da página</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <p>Eu sou um paragrafo</p>
  </body>
</html>
{% endhighlight %}

style.css
{% highlight css %}
p{
  color: blue;
}
{% endhighlight %}

* Aconselhável utilizar sempre desse modo, css valerá para todo o projeto, diminui o trabalho e retrabalho de forma imensurável.

<h3 style="color: blue; text-align: center;">CSS - Estrutura básica</h3>

A estrutura de um CSS é:

{% highlight css %}
p {
  color: blue;
}
{% endhighlight %}

<h4 style="color: red;">Explicação da estrutura</h4>

<img src="/assets/imagens/css/aula_um/declaracao_css.png"/>

O CSS usa seletores para etilizar um elemento, as principais formas de etilizar um elemento são:

- Seletor de elemento: p, h1, etc.
- Seletor de classe: .titulo, .white, etc.
- Seletor de id: #secao_um, #titulo_um.

- O seletor de elemento valerá para todos os elementos selecionados.
- O seletor de classe valerá para todos os elementos que tiver a classe selecionada.
- O seletor de id valerá para um único elemento, que terá o id informado.

<h4 style="color: red;">O que veremos</h4>

Neste artigo veremos:

- Colors
- Backgrounds
- Border
- Margin
- Padding

Para fazermos alguns exemplos. Crie uma pasta no seu desktop chamada "css", dentro dela outra chamada "aula_um".

Abra o editor de texto que está utilizando e salve um arquivo como "index.html".

Se estiver usando o Notepad++, vá em:

- Arquivo
- Salvar como
- Encontre a pasta aula_um
- Coloque como nome index.html
- Mude o tipo para Hyper Text Markup Language
- Salve

Depois salve um arquivo chamado "style.css".

Clique 2 vezes no arquivo index.html para que ele seja aberto no navegador.

Escreva no index.html
{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>Título da página</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <section id="secao_um">
      <h1>Eu sou um titulo</h1>
      <p class="red">Eu sou um paragrafo</p>
      <h2 id="sienna">Eu sou um sub-titulo</h2>
      <p class="green">Eu sou um paragrafo</p>
    </section>
    <section id="secao_dois">
      <h1>Eu sou um titulo</h1>
      <p class="red">Eu sou um paragrafo</p>
      <h2>Eu sou um sub-titulo</h2>
      <p class="green">Eu sou um paragrafo</p>
    </section>
    <section id="secao_tres">
      <h1>Eu sou um titulo</h1>
      <p class="red">Eu sou um paragrafo</p>
      <h2>Eu sou um sub-titulo</h2>
      <p class="blue">Eu sou um paragrafo</p>
    </section>
    <section id="secao_quatro">
      <h1>Eu sou um titulo</h1>
      <p class="red">Eu sou um paragrafo</p>
      <h2>Eu sou um sub-titulo</h2>
      <p class="blue">Eu sou um paragrafo</p>
    </section>
  </body>
</html>
{% endhighlight %}

Olhando esse código conseguimos perceber que separamos o html por section, sendo assim vamos estilizar eles primeiro. A cada vez que colocar um código, salve o arquivo e atualize o navegador.

<h4 style="color: red;">Antes de estilizar</h4>

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/antes.JPG"/>
</div>

<h4 style="color: red;">Background</h4>

style.css
{% highlight css %}
#secao_um, #secao_tres {
  background-color: #A9A9A9;
}

#secao_dois, #secao_quatro {
  background-color: #DCDCDC;
}
{% endhighlight %}

* Quando 2 seletores diferentes tem a mesma declaração, separamos eles por "," para escrever 1 vez só.

<h4 style="color: red;">Color</h4>

O atributo color tem alguns valores de cores possíveis:
- Hexadecimal
- RGB

Tem uma lista [aqui](http://erikasarti.com/html/tabela-cores/).

{% highlight css %}
h1{
  color: #FFA500;
}
{% endhighlight %}

* Os seletores de elementos são chamados diretamente.

{% highlight css %}
.red{
  color: red;
}
.green{
  color: green;
}
.blue{
  color: blue;
}
{% endhighlight %}

* Os seletores de classe tem o "." na frente.

{% highlight css %}
#sienna{
  color: rgb(160,82,45);
}
{% endhighlight %}

* Os seletores de id tem o "#" na frente.

<h4 style="color: red;">Border</h4>

A border tem os seguintes valores:
- Largura da borda
- Tipo da borda
- Cor da borda

{% highlight css %}
#secao_um{
  border: 10px solid #000;
}

#secao_dois{
  border: 10px solid #FF69B4;
}

#secao_tres{
  border: 10px solid #000080;
}

#secao_quatro{
  border: 10px solid #800000;
}
{% endhighlight %}

<h4 style="color: red;">Padding</h4>

O padding é o espaço dentro de um elemento, entre a borda e o conteúdo.

{% highlight css %}
section{
  padding: 3%;
}
{% endhighlight %}

<h4 style="color: red;">Margin</h4>

O margin é o espaço fora de um elemento, entre um elemento e outro.

{% highlight css %}
body{
  margin: 0;
}
{% endhighlight %}

- Tiramos a borda natural que tem dentro da body, assim encostando os elementos nas boras da tela.

<h4 style="color: red;">Depois de estilizar</h4>

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/depois.png"/>
</div>

Este foi um artigo com alguns conceitos básicos de CSS, continue acompanhando o blog que terá muito mais.

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/front-end/html/html-parte-um-conceitos-basicos.html">HTML - Parte I - Conceitos básicos</a></div><div style="float: right"><a href="https://programadoresreais.com.br/front-end/html/html-parte-dois-conceitos-basicos.html">Próximo: HTML - Parte II - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte I
- JavaScript - Parte I
- CPanel - Guia definitivo
- Resenha: Livro A Lei de Murphy no Gerenciamento de projetos

<br><br>
Comentem aqui em baixo, marquem gostei, tirem dúvidas, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>

{% include disqus.html %}
