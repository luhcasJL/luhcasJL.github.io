---
layout: post
title:  "HTML - Parte 3 - Conceitos básicos"
date:   2019-03-26 12:10:53 -0200
categories: front-end/html
permalink: /:categories/:title.html
author: "Lucas"
description: "Vídeo, Áudio, YouTube, Atributo hidden"
---


Boas devs, para o artigo de hoje vamos tratar sobre multimídia.

<div style="text-align: center;">
  <img src="/assets/imagens/html/aula_tres/midias.png"/>
</div>

Por que este definitivamente foi a parte mais esperada no HTML, e que enterrou de vez o flash player e seus problemas de segurança. 10 segundos de silêncio.

<div style="text-align: center;">
  <img src="/assets/imagens/html/aula_tres/flash.jpg"/>
</div>

Chega de enrola, no artigo de hoje veremos como se utiliza:

- Vídeo
- Áudio
- YouTube
- Atributo hidden

<h4 style="color: red;">Vídeo</h4>

Os vídeos são chamados com a tag "video" e seguido da tag "source".

{% highlight html %}
<video width="640" height="360" controls poster="video.jpg">
  <source src="video.mp4" type="video/mp4">
  <source src="video.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
{% endhighlight %}

<div style="text-align: center;">
  <video width="640" height="360" controls poster="/assets/imagens/html/aula_tres/video.JPG">
    <source src="/assets/imagens/html/aula_tres/video.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

A tag "video" pode receber alguns atributos importantes tais como:

- controls: implementa as opções de controle de vídeo (iniciar, pausar, volume, etc).
- poster: define uma imagem de proteção que será mostrada antes do vídeo ser iniciado.
- autoplay: define que o vídeo se iniciara assim que a página for carregada.
- loop: define que o vídeo será reiniciado sempre que chegar ao final.
- muted: define que o vídeo iniciara mudo.
- width e height: definem largura e altura do vídeo, aconselhável ser definido pelo css.

A tag "source" vem com os atributos:

- src: define o caminho do arquivo.
- type: define o tipo e o formato do arquivo.

Pode ser colocado mais do que um source, que caso o navegador não consiga pegar o primeiro ele tenta os próximos.

Não funciona muito bem no ambiente local, só quando está hospedado.

<h4 style="color: red;">Áudio</h4>

Os vídeos são chamados com a tag "video" e seguido da tag "source".

{% highlight html %}
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
{% endhighlight %}

<audio controls>
  <source src="/assets/imagens/html/aula_tres/audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

A tag "audio" pode receber alguns atributos importantes tais como:

- controls: implementa as opções de controle de vídeo (iniciar, pausar, volume, etc).
- autoplay: define que o vídeo se iniciara assim que a página for carregada.
- loop: define que o vídeo será reiniciado sempre que chegar ao final.
- muted: define que o vídeo iniciara mudo.
- width e height: definem largura e altura do vídeo, aconselhável ser definido pelo css.

A tag "source" vem com os atributos:

- src: define o caminho do arquivo.
- type: define o tipo e o formato do arquivo.

<h4 style="color: red;">YouTube</h4>

Para colocar vídeos do YouTube pode pegar o código diretamente do site. Na opção "compartilhar", tem a opção "embed", cópie o código passado.

{% highlight html %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/swTki-Klk3g" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
{% endhighlight %}

<div style="text-align: center;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/swTki-Klk3g" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

Também podemos chamar por outra tag.

{% highlight html %}
<embed width="420" height="315" src="https://www.youtube.com/embed/swTki-Klk3g">
{% endhighlight %}

<div style="text-align: center;">
  <embed width="420" height="315" src="https://www.youtube.com/embed/swTki-Klk3g">
</div>

A primeira opção dá menos trabalho e eu prefiro.

<strong>Antes de encerra este artigo, peço que não seja o tipo de pessoa que coloca "autoplay hidden" juntos nos áudios ou vídeos do seu site, além de ser super chato as pessoas sumirão.</strong>

E já que falamos na tag hidden.

<h4 style="color: red;">Hidden</h4>

Ela é utilizada para deixar algum elemento "escondido" na página, existe, mas não é mostrado, pode não parecer, mas é muito útil no desenvolvimento.

{% highlight html %}
<source src="/assets/imagens/html/aula_tres/audio.mp3" type="audio/mpeg" hidden>
{% endhighlight %}

Então é isto, estamos chegando ao fim de "HTML - Conceitos básicos", o próximo artigo será sobre formulários e depois iniciaremos a construção de layouts completos.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/front-end/css/css-parte-dois-conceitos-basicos.html">CSS - Parte 2 - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/front-end/css/css-parte-tres-conceitos-basicos.html">CSS - Parte 3 - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte 3 - Conceitos básicos
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
