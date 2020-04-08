---
layout: post
title:  "HTML - Parte 4 - Conceitos básicos"
date:   2019-03-29 12:23:53 -0200
categories: front-end/html
permalink: /:categories/:title.html
author: "Lucas"
description: "Iframes, formulários, tabelas"
---

Boas devs, esta é a última parte sobre os "Conceitos Básico de HTML", em breve iniciaremos construções de layouts.

<div style="text-align: center;">
  <img src="/assets/imagens/html/html.png"/>
</div>

Para o artigo de hoje temos:

- Iframe
- Forms

<h4 style="color: red;">Iframe</h4>

O iframe é um display que contém uma página externa, por exemplo chamar o site do google dentro do seu site.

{% highlight html %}
<iframe src="http://example.com" style="height:300px;width:100%; border:0;"></iframe>
{% endhighlight %}


Eu sinceramente não sei por que alguém faria isso, até porque a maioria dos sites bloqueiam ser chamados por iframe.

<h4 style="color: red;">Formulários</h4>

O formulário é uma das partes mais importantes de um projeto, a partir dele conseguimos que o cliente converse conosco, ou interaja melhor com o sistema e com o banco de dados.

{% highlight html %}
<form action="" method=""></form>
{% endhighlight %}

Vamos considerar neste artigo o seguinte código

{% highlight html %}
<form action="recebe.html" method="">
  <label for="nome">Nome:</label><br>
  <input type="text" name="nome" id="nome" value=""><br>
  <label for="sobrenome">Sobrenome:</label><br>
  <input type="text" name="sobrenome" id="sobrenome" value=""><br><br>
  <input type="submit" name="" value="enviar">
</form>
{% endhighlight %}

O form tem por padrão dois atributos, a "action" e o "method".

<h4 style="color: red;">Action</h4>

A "action" recebe o caminho para onde as informações devem ser enviadas.

{% highlight html %}
<form action="recebe.html" method=""></form>
{% endhighlight %}

<h4 style="color: red;">Method</h4>

O "method" pode receber 2 parâmetros:

- get
- post

<h4 style="color: green;">Parâmetro get</h4>

O formulário com o parâmetro "get" envia os dados usando a "url" do site.

Considere o seguinte código:

{% highlight html %}
<form action="recebe.html" method="get"></form>
{% endhighlight %}

<div style="text-align: center;">
  <img src="/assets/imagens/html/aula_quatro/formulario_get.JPG"/>
</div>

Quando enviarmos esse formulário ele será recebido pela pagina "recebe.html" pelo link.

{% highlight html %}
recebe.html?nome=Lucas&sobrenome=Alves
{% endhighlight %}

Esse é um método bastante inseguro, já que as informações ficam visíveis e salvos no histórico do navegador, NUNCA use "get" para enviar senhas ou informações sensíveis.

<h4 style="color: green;">Parâmetro post</h4>

O parâmetro "post" envia os dados sem passar pela "url", desta forma fica mais seguro o envio.

{% highlight html %}
<form action="recebe.html" method="post"></form>
{% endhighlight %}

<strong>Para utilizar as informações enviadas pelo "get" ou "post" será necessário o uso de alguma linguagem de programação, será falado nos artigos de JavaScript e PHP.</strong>

<h4 style="color: red;">Elementos</h4>

Alguns elementos de um formulário são:

- label
- input
- select
- textarea

<h4 style="color: red;">Label</h4>

A tag "label" serve para identificar o campo input, ela também pode receber o atributo "for" que serve para identificar a qual input pertence.

Quando o usuário clicar no "label" nome, o input com o "id" nome ficará com a borda azul brilhante.

<h4 style="color: red;">Input</h4>

O "input" é onde colocamos as informações a serem enviadas. A estrutura básica é:

{% highlight html %}
<input type="" name="" id="" class="" value="">
{% endhighlight %}

<h4 style="color: green;">Name</h4>

É o atributo que identifica cada "input" na hora de tratar as informações recebidas.

<h4 style="color: green;">ID</h4>

O "id" é um identificador único, é muito útil para fazer validações pelo JavaScript antes de enviar o formulário e também é utilizado para identificação do "for". Pegue o hábito de sempre colocar o "id".

<h4 style="color: green;">Class</h4>

A "class" é comumente utilizada para fazer estilizações pelo CSS.

<h4 style="color: green;">Value</h4>

A "value" costuma ficar vazia, ela só é preenchida quando queremos deixar uma informação já preenchida.

<h4 style="color: green;">Type</h4>

O "type" serve para identificar qual tipo de input teremos.

Alguns tipos são:

- <strong>text</strong> - do tipo texto
- <strong>number</strong> - do tipo número (só aceita números)
- <strong>password</strong> - esconde as informações digitadas
- <strong>email</strong> - do tipo email
- <strong>date</strong> - do tipo data (chama um calendário)
- <strong>reset</strong> - limpa todos os campos dentro do formulário
- <strong>submit</strong> - envia o formulário

Outros tipos são:

- <strong>file</strong> - serve para receber documentos
- <strong>checkbox</strong> - a caixinha de marcar coisas

{% highlight html %}
<form action="recebe.html" method="post">
  Cores preferidas:<br><br>
  <input type="checkbox" name="cor[]" id="" class="tipo_cor" value="azul"><label for="azul">Azul</label><br>
  <input type="checkbox" name="cor[]" id="" class="tipo_cor" value="vermelho"><label for="">Vermelho</label><br>
  <input type="checkbox" name="cor[]" id="" class="tipo_cor" value="verde"><label for="">Verde</label><br>
</form>
{% endhighlight %}

- <strong>radio</strong> - neste tipo só se pode escolher 1 opção

{% highlight html %}
<form action="recebe.html" method="post">
  Gênero:<br><br>
  <input type="radio" name="genero" value="Masculino"> Masculino<br>
  <input type="radio" name="genero" value="Feminino"> Feminino<br>
</form>
{% endhighlight %}


<h4 style="color: red;">Select</h4>

O "select" trás uma lista para ser selecionado um elemento.

{% highlight html %}
<form action="recebe.html" method="post">
  Escolha um tema:<br><br>
  <select name="cars">
    <option value="tema_um">Tema 1</option>
    <option value="tema_dois">Tema 2</option>
    <option value="tema_tres">Tema 3</option>
    <option value="tema_quatro">Tema 4</option>
  </select>
</form>
{% endhighlight %}

<h4 style="color: red;">Text area</h4>

O "textarea" consegue receber mais informações que um input text.

{% highlight html %}
<form action="recebe.html" method="post">
  Mensagem:<br><br>
  <textarea name="name" rows="8" cols="80"></textarea>
</form>
{% endhighlight %}

<h4 style="color: red;">Atributos formulário</h4>

Temos alguns atributos que podemos colocar nos elementos do formulário.

- <strong>readonly</strong> - campo não pode ser alterado, só fica para leitura
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" readonly>
{% endhighlight %}
- <strong>disabled</strong> - campo fica desativado
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" disabled>
{% endhighlight %}
- <strong>size</strong> - tamanho do input, recomendo fazer por CSS
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" size="40">
{% endhighlight %}
- <strong>maxlength</strong> - máximo de caracteres aceitos
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" maxlength="10">
{% endhighlight %}
- <strong>minlenght</strong> - mínimo de caracteres aceitos
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" minlenght="3">
{% endhighlight %}
- <strong>autofocus</strong> - quando carrega a página, o cursor já fica marcado para digitar
{% highlight html %}
  <input type="text" name="nome" id="nome" value="Lucas" autofocus>
{% endhighlight %}


E termina assim os "Conceitos Básicos de HTML", nestes 4 artigos cobrimos uma boa parte do que o HTML pode fazer e das "tags" mais utilizadas na maioria dos sites.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/front-end/css/css-parte-tres-conceitos-basicos.html">CSS - Parte 3 - Conceitos básicos</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/front-end/css/css-parte-quatro-conceitos-basicos.html">CSS - Parte 4 - Conceitos básicos</a></div>

<br><br>
Planejamento de artigos:
- CSS - Parte 4 - Conceitos básicos
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
