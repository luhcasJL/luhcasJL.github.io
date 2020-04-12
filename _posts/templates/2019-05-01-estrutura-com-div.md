---
layout: post
title:  "Estrutura com div"
date:   2019-05-01 11:39:00 -0200
categories: templates
permalink: /:categories/:title.html
author: "Lucas"
description: "Tableless, conceito de div, estrutura padrão"
---

Boas devs,

Primeiramente venho explicar que o blog não morreu, estava apenas em sono profundo devido eu estar bastante ocupado (graças a Deus) em um projeto importante.

Este artigo vai dedicado aos Janderson, Júlio e Evanndro pelo pedido de uma explicação sobre divs, então vamos nessa.

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/w3c.png" style="height: 200px; "/>
</div>

Quando nos deparamos com uma estrutura assim:

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/um.png"/>
</div>

Somos tentados a fazer algo assim:

{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <table border="1" width="80%" style="position: relative; left: 10%;">
      <tr style="height: 150px;">
        <td colspan='3'></td>
      </tr>
      <tr style="height: 150px;">
        <td colspan='3'></td>
      </tr>
      <tr style="height: 250px;">
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr style="height: 150px;">
        <td colspan='3'></td>
      </tr>
    </table>
  </body>
</html>
{% endhighlight %}

E chegaremos ao resultado esperado:

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/dois.PNG"/>
</div>

<br>
Mas isso não é o correto a se fazer, e devido a isso a W3C "World Wide Web Consortium" principal empresa que define os padrões para criação e interpretações de conteúdos web, fez um comunicado de que cada "tag" deve ser utilizada para o proposito dela, e que a "table" deve ser usada para apresentação de conteúdo tabulado e não para criar estruturas.

Sendo assim, foi criada uma forma de desenvolvimento chamada tableless "menos tabela".

Explicado o por quê não fazer do modo acima, vamos a melhor solução até o momento.

<h4 style="color: red;">DIV - Divisores</h4>

A tag "div" serve como o nome sugere, para fazer divisões na página, vamos ao exemplo acima e fazer um código do modo correto.

O html ficará assim, eu coloquei o nome das divs de forma que não precise de muita explicação de qual div representa qual área.

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

Apenas este código não resolve muito, precisamos fazer os ajustes necessários utilizando CSS.

Vamos ponto a ponto.

{% highlight css %}
.conteudo{
  width: 65%;
  margin: 0 auto;
  text-align: center;
  font-size: 1.5rem;
}
{% endhighlight %}

Primeiro peguei a div que corresponde a todo o conteúdo que será apresentado, defini como 65% de largura e centralizei com o margin.

{% highlight css %}
.cabecalho{
  width: 100%;
  height: 100px;
  border: 1px solid #000;
}

.banner{
  width: 100%;
  height: 250px;
  border: 1px solid #000;
}

.areas{
  width: 100%;
  height: 315px;
  border: 1px solid #000;
}
{% endhighlight %}

Ao cabeçalho, defini a largura e a altura do elemento, a borda coloquei para melhorar a visualização dos elementos criados, mesma coisa pro banner e para o areas.

Na área "areas" existem 3 elementos.

{% highlight css %}
.area_esquerda, .area_central, .area_direita{
  float: left;
  height: 315px;
  width: 33%;
  border: 1px solid #000;
}

.area_esquerda, .area_central{
  margin-right: 0.20%;
}
{% endhighlight %}

Para que todos eles fiquem ao lado do outro, defini um "float: left", defini altura e largura, dividindo por "," para valer para os 3.

Logo em seguida, para que ocupe todo o espaço horizontal, dei um margin-right de 0,20% nos dois primeiros elementos.

{% highlight css %}
.rodape{
  width: 100%;
  height: 100px;
  border: 1px solid #000;
}
{% endhighlight %}

Ao rodapé, já foi explicado lá em cima.

O resultado final foi:

<div style="text-align: center;">
  <img src="/assets/imagens/templates/div/tres.PNG" style="height: 500px;"/>
</div>
<br>

<h4 style="color: red;">Vantagens</h4>

- O código fica semanticamente correto
- Os navegadores conseguem renderizar melhor
- O buscadores entendem e aumenta
- Aumenta as chances de serem encontrados pelos navegadores
- Pode ficar responsivo

Este exemplo não foi feito usando responsividade já que o intuito inicial é mostrar como funciona as estruturas usando div.

Eu reescrevi o html de forma semântica, [leia aqui](https://programadoresreais.com.br/templates/estrutura-html-semantico.html).

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/front-end/css/css-parte-cinco-conceitos-basicos.html">CSS Parte 5 - Conceitos Básicos</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/templates/estrutura-html-semantico.html">Estrutura com html semântico</a></div>

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
