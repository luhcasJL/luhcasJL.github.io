---
layout: post
title:  "CSS - Parte 2 - Conceitos básicos"
date:   2019-03-22 12:12:53 -0200
categories: front-end/css
permalink: /:categories/:title.html
author: "Lucas"
description: "Unidades de medidas"
---

Boas devs, essa é a parte 2 da série CSS - Conceitos Básicos e continuação da série que pretende tornar-te desenvolvedor Full Staaaaack.

<div style="text-align: center;">
  <img src="/assets/imagens/css/aula_um/css.jpeg"/>
</div>

<br>

No artigo [anterior](https://programadoresreais.com.br/front-end/css/css-parte-um-conceitos-basicos.html) aprendemos as formas de implementar o CSS, alguns conceitos iniciais e estilização de uma página de conteúdo.

Neste artigo vou ensinar um conceito muito importante chamado "Unidades de medidas", o texto é um pouco longo, mas será essencial para não se perder no futuro.

Dito isto, coisas que veremos neste artigo:

- Unidades de medidas

<h3 style="color: blue; text-align: center;">Unidades de medidas</h3>

No artigo anterior deve ter percebido o uso de "px". Mas será que só existe ele? Certamente não e hoje explicarei para que servem as unidades de medidas.

Existem duas áreas, sendo:

- Unidades de medidas de distância
- Unidades de medidas para outras quantidades

<h4 style="color: red;">Unidades de medidas de distância</h4>

  As unidades de medidas de distância definem medidas na horizontal, vertical ou qualquer outra direção, elas são divididas em:

  - Medidas absolutas
  - Medidas relativas

<h4 style="color: green;">Medidas absolutas</h4>

As medidas absolutas são aquelas que não mudam seu tamanho seja lá qual for o display utilizado, elas também são conhecidas pelo uso da física.

- cm (centímetro) = 96px/2.54;
- mm (milímetro) = 1/10cm;
- q (1/4 do milímetro) = 1/40cm;
- in (polegada) = 2,54cm = 96px;
- pc (pica) = 12 points ou 1/6in;
- pt (point) = 1/72in;
- px (pixel) = 1/96in;

Obs.: Desta lista eu só utilizei o px até hoje, mas vale conhece-las para saber como usar no momento oportuno, <strong>elas só devem ser utilizadas em projetos que a tela do computador não muda</strong>.

Exemplo: Temos um monitor de 1280 x 800 e definimos uma div com "width: 1280px;" e "height: 800px;".

- width = largura
- height = altura.

Neste exemplo ocupamos toda a parte visual do monitor, agora imagine se alguém abrir a página em um monitor de 1024 x 728, acontecerá neste caso que a página ultrapassará o tamanho e criará a barra horizontal para que a tela seja "movida";

<h4 style="color: green;">Medidas relativas</h4>

As medidas relativas são muito utilizadas no desenvolvimento responsivo, elas dão tamanho as coisas com base a outra unidade de medida e ao tamanho do display utilizado no momento, se bem utilizadas se tornam altamente adaptativas.

<strong>rem</strong>: calculado pelo tamanho da fonte do elemento raiz do documento, geralmente os navegadores tem fonte padrão de 16px.

No exemplo abaixo o paragrafo terá como tamanho da fonte 16 x 1.5 = 24px.

{% highlight css %}
p{
  font-size: 1.5rem;
}
{% endhighlight %}

<strong>em</strong>: calculado pelo tamanho da fonte do elemento no qual a unidade é declarada;

No exemplo abaixo o paragrafo terá como tamanho da fonte 20 x 1.5 = 30px.

{% highlight html %}
<div class="div_um">
  <p class="paragrafo_um">Eu sou um paragrafo</p>
</div>
{% endhighlight %}

{% highlight css %}
.div_um {
  font-size: 20px;
}

.paragrafo_um {
  font-size: 1.5em;
}
{% endhighlight %}

Obs.: Se a div estivesse definida com 1.5rem, o calculo seria 16 x 1.5 = 24px para div e 24 x 1.5 = 36px para paragrafo.

<strong>ex</strong>: ...a altura da letra x (xis) da fonte herdada;

<strong>ch</strong>: ...a largura acrescida do espaçamento em volta do número 0 (zero) da fonte do elemento no qual a unidade é declarada;

<strong>Obs.: Eu utilizei font-size como exemplo, mas pode ser utilizado qualquer propriedade de definição de tamanho. Na dúvida usa o rem. ^^</strong>

Temos também para medidas relativas:

<strong>vw</strong>: valor largura da viewport;

Se queremos que um elemento ocupe metade da largura do display utilizamos:

{% highlight css %}
.div_um{
  height: 50vw;
}
{% endhighlight %}

Confesso que não o conhecia até agora, o que não faz muito sentido já que eu uso bastante o vh, fiquei animado em fazer uns testes de media querys nele. ^^

<strong>vh</strong>: valor altura da viewport;

Esse é um que gosto muito, se queremos que um elemento ocupe metade da altura do display utilizamos:

{% highlight css %}
.div_um{
  height: 50vw;
}
{% endhighlight %}

<strong>vmin</strong>: a menor medida entre vw e vh;

<strong>vmax</strong>: a maior medida entre vw e vh.

<strong>%</strong>: dizem que não é unidade de medida e sim tipo de dado, mas é muito utilizado pra fazer os layouts se comportarem de forma adequada.

{% highlight css %}
.div_um{
  height: 50%;
}
.div_dois{
  height: 50%;
}
{% endhighlight %}

Sempre utilizei assim, acho que por isso o "vw" me passou despercebido durante todo esse tempo.

<h4 style="color: red;">Unidades de medidas para outras quantidades</h4>

- Ângulos
- Duração
- Frequência
- Resolução

<h4 style="color: green;">Ângulos</h4>

- deg (grau): um círculo tem 360deg;
- grad (grado): um círculo tem 400grad;
- rad (radiano): um círculo tem 2𝛑rad;
- turn (volta): um círculo tem 1turn;

{% highlight html %}
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
    <style media="screen">
      .um, .dois, .tres, .quatro, .cinco, .seis, .sete{
        height: 50px;
        width: 50px;
        border: 3px solid #FF0000;
        background-color: #0000FF;
        margin: 30px;
        color: white;
      }

      .dois{
        transform: rotate(45deg);
      }

      .tres{
        transform: rotate(60deg);
      }

      .quatro{
        transform: rotate(-30deg);
      }

      .cinco{
        transform: rotate(250grad);
      }

      .seis{
        transform: rotate(25rad);
      }

      .sete{
        transform: rotate(0.5turn);
      }
    </style>
  </head>
  <body>
    <div class="um">um</div>
    <div class="dois">dois</div>
    <div class="tres">tres</div>
    <div class="quatro">quatro</div>
    <div class="cinco">cinco</div>
    <div class="seis">seis</div>
    <div class="sete">seis</div>
  </body>
</html>
{% endhighlight %}

Vai brincando ai e vendo como funciona, o "deg" é o mais usado.

<h4 style="color: green;">Duração</h4>

- s (segundo): 1s;
- ms (milissegundo): 1/1000s;

Usa o mesmo arquivo que testou o código de cima.

{% highlight css %}
.um{
  animation: roll 8s infinite;
}

@keyframes roll {
  0% {
    transform: rotate(0);
  }
  5% {
    position: relative;
    left: 5vw;
  }
  20% {
    position: relative;
    left: 20vw;
  }
  35% {
    position: relative;
    left: 35vw;
  }
  50% {
    position: relative;
    left: 50vw;
  }
  65% {
    position: relative;
    left: 65vw;
  }
  85% {
    position: relative;
    left: 85vw;
  }
  100% {
    transform: rotate(-360deg);
  }
}
{% endhighlight %}

Eu sei que é muito, muito legal animar as coisas, mas cautela. (E não é que eu achei um uso significativo por "vw").

<h4 style="color: green;">Unidades para frequência</h4>

- Hz (Hertz) - número de ocorrências por segundo;
- kHz (KiloHertz) - 1000Hz;

<h4 style="color: green;">Unidades para resolução</h4>

- dpi (dots per inch) - pontos por polegada;
- dpcm (dots per centimeter) - pontos por centímetro;
- dppx (dots per pixel) - pontos por pixel;

<br>

Então foi isso por hoje amigos, no próximo uma explicação mais aprofundada dos tópicos apresentados no artigo anterior:

- Colors
- Backgrounds
- Border
- Margin
- Padding

Além de ser muito bom pra melhorar o CSS dará mais tempo pro avanço do HTML, o CSS não pode passar a frente do conhecimento em HTML. Em breve faremos layouts lindos.

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/front-end/html/html-parte-dois-conceitos-basicos.html">HTML - Parte I - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/front-end/html/html-parte-tres-conceitos-basicos.html">HTML - Parte 3 - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- HTML - Parte 3 - Conceitos básicos
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
