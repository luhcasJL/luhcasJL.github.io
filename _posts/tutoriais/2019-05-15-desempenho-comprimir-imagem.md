---
layout: post
title:  "Desempenho - Comprimir imagem"
date:   2019-05-15 16:16:53 -0200
categories: tutoriais
permalink: /:categories/:title.html
author: "Lucas"
description: "Comprimir imagem com TinyPNG"
---

Boas devs,

No artigo de hoje vou mostrar uma forma de comprimir imagens sem perder a qualidade a as vantagens que isso tem.

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/dez.jpg"/>
</div>
<br>

Para este artigo eu vou utilizar o projeto que eu disponibilizei no artigo sobre [hospedagem](https://lucasalves.ml/tutoriais/hospedagem-guia-definitivo.html){:target='blank' rel='noopener'} ele está no [GitHub](https://github.com/luhcasJL/blog/tree/master/portfolio){:target='blank' rel='noopener'} e hospedado [aqui](http://tutorialhospedagem.dx.am/){:target='blank' rel='noopener'}.

Vamos trabalhar apenas na página inicial, começando com alguns testes de desempenho.

O primeiro é a medição do próprio navegador:

- Clique no botão direito do mouse e selecione inspecionar
- Vá na aba Network
- Clique no símbolo de bloqueio para limpar
- Marque a opção disabled cache

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/um.PNG"/>
</div>
<br>

- ctrl + shift + r para recarregar a página limpando o cache

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/dois.PNG"/>
</div>
<br>

Dar um zoom para ver melhor os dados

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/tres.PNG"/>
</div>
<br>

O carregamento da página com todos os arquivos está levando 4.31 segundos.

Agora vamos pegar a nota no [pagespeed](https://developers.google.com/speed/pagespeed/insights/){:target='blank' rel='noopener'}

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/cinco.PNG"/>
</div>
<br>

A nota pode parecer alta, mas leve em consideração que só tem 6 imagens na página.

Agora vamos ao [TinyPNG](https://tinypng.com/){:target='blank' rel='noopener'}, ele é bem simples de se usar, você pega os arquivos e colocam lá e ele faz automático.

O legal do TinyPNG é que ele comprimi a imagem sem perder a qualidade, mas é muito importante que a pessoa guarde as imagens originais, pois as que foram comprimidas não são boas para edição, se editar elas, a qualidade será perdida.

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/sete.PNG"/>
</div>
<br>

Veja imagem a imagem a diferença da compressão e que a compressão total ficou em 57%, isso já vai diminuir bastante o tempo de carregamento da página, vou hospedar as novas e fazer novamente os testes. Aah, faça o download das novas imagens e coloque na pasta correspondente.

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/oito.PNG"/>
</div>
<br>

O carregamento da página que tinha levado 4.31 segundos passou para 2.33 segundos, isso é uma diferença bem considerável.

Pagespeed

<div style="text-align: center;">
  <img src="/assets/imagens/tutorial/comprimir/nove.PNG"/>
</div>
<br>

Fomos de 86 pontos para 90, mas veja um ponto importante, saímos do laranja para o verde e isso conta bastante para o rankeamento do google.

Infelizmente precisa explicar que existem diversas outras maneiras, em algumas situações de forma mais eficiente, mas que este blog é feito para pessoas que precisam aprender algo e não para os enciclopédias da vida.

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

<div style="display: inline;">Anterior: <a href="https://lucasalves.ml/logica-programacao/logica-programacao-parte-dois.html">Lógica de programação - Parte 2</a></div><div style="float: right">Próximo: <a href="https://lucasalves.ml/negocios/contratos-voce-deve-fazer.html">Contratos - Você deve fazer</a></div>

<br><br>
Comentem aqui em baixo, marquem gostei, tirem dúvidas, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>

{% include disqus.html %}
