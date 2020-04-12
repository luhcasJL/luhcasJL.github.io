---
layout: post
title:  "HTML - Parte 1 - Conceitos básicos"
date:   2019-03-18 14:14:53 -0200
categories: front-end/html
permalink: /:categories/:title.html
author: "Lucas"
description: "Definição, Implementação, Estrutura básica, Títulos, Parágrafos, Links, Quebra de linha, Botão, Lista não ordenada, Lista ordenada, Tabela, DIV"
---

Boas devs, começando a série de artigos que tem o intuito de tornar-te um desenvolvedor Full Stack.

<h3 style="color: blue; text-align: center;">HTML - Definição</h3>

Hyper Text Markup Language (HTML) ou Linguagem de marcação de texto foi desenvolvido por Tim Berners-Lee em sua primeira versão em 1991, atualmente estamos na versão 5.

Em poucas palavras o HTML serve para fazer a estrutura (esqueleto) de um website.

Podemos escrever o html utilizando diversos editores de texto, sendo eles:

- Bloco de notas do computador
- [Notepad++](https://notepad-plus-plus.org/download/v7.6.4.html)
- [Atom](https://atom.io/)
- [SublimeText](https://www.sublimetext.com/)

Recomendo por agora utilizar o Notepad++ porque tem menos recursos de completar código, sendo assim você memoriza eles mais facilmente.

Vamos começar a primeira página. Crie uma pasta no seu desktop chamada "html", dentro dela outra chamada "aula_um".

Abra o editor de texto que está utilizando e salve um arquivo como "index.html".

Se estiver usando o Notepad++, vá em:

- Arquivo
- Salvar como
- Encontre a pasta aula_um
- Coloque como nome index.html
- Mude o tipo para Hyper Text Markup Language
- Salve

Os arquivos HTML são salvos com ".html" ou ".htm"

<h3 style="color: blue; text-align: center;">HTML - Estrutura básica</h3>

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>Título da página</title>
  </head>
  <body>

  </body>
</html>
{% endhighlight %}

<h4 style="color: red;">Explicação da estrutura</h4>

{% highlight html %}
- <!DOCTYPE html> - Diz que iremos usar o HTML5
- <html></html> - Define que dentro dele será considerado HTML até que tenha uma instrução diferente
- <head></head> - Define a "cabeça da página", aqui definimos o título da página, o idioma a ser considerado, etc
- <title></title> - Define o título da página, aquele que será mostrado na aba do navegador
- <body></body> - Define o "corpo da página", aqui que é colocado todo o código a ser apresentado na tela
{% endhighlight %}

Em sua grande maioria, as tags deverão serem abertas e fechadas.
<tag></tag>

As tags não fechadas serão explicadas ao avançar da série.

Vá ao seu arquivo index.html e escreva (escreva, não copie e cole):

Deverão ser escritos dentro do body

<h4 style="color: red;">Títulos</h4>

{% highlight html %}
<h1>Eu sou um título tamanho H1</h1>
<h2>Eu sou um sub-título tamanho H2</h2>
<h3>Eu sou um sub-título tamanho H3</h3>
<h4>Eu sou um sub-título tamanho H4</h4>
<h5>Eu sou um sub-título tamanho H5</h5>
<h6>Eu sou um sub-título tamanho H6</h6>
{% endhighlight %}

Salve o arquivo (CRTL+S), vá no arquivo index.html e abra ele (ele será aberto no navegador padrão, Google Chrome, Firefox, etc)

Em seguida coloque abaixo dos títulos, a cada vez que colocar algo novo, salve o arquivo com CRTL+S e atualize a página no navegador.

<h4 style="color: red;">Parágrafos</h4>

{% highlight html %}
<p>Eu sou um paragrafo.</p>
<p>Eu sou outro paragrafo.</p>
{% endhighlight %}

<h4 style="color: red;">Links</h4>

{% highlight html %}
<a href="https://programadoresreais.com.br/">Eu sou um link</a>
{% endhighlight %}

- a tag link tem o atributo href para referenciar o caminho a ser levado.

<h4 style="color: red;">Quebra de linha</h4>

{% highlight html %}
<br>
{% endhighlight %}

- A tag <b>br</b> é uma quebra de linha na página, ele não tem fechamento de tag
- As tags de título e paragrafo ocupem a linha inteira, então não precisam do <b>br</b>.

<h4 style="color: red;">Botão</h4>

{% highlight html %}
<button>Eu sou um botão</button>
{% endhighlight %}

<h4 style="color: red;">Lista não ordenada</h4>

{% highlight html %}
<h4>Abaixo uma lista não ordenada</h4>
<ul>
  <li>Aula 1</li>
  <li>Aula 2</li>
  <li>Aula 3</li>
</ul>
{% endhighlight %}

<h4 style="color: red;">Lista ordenada</h4>

{% highlight html %}
<h4>Está é uma lista ordenada</h4>
<ol>
  <li>Aula 1</li>
  <li>Aula 2</li>
  <li>Aula 3</li>
</ol>
{% endhighlight %}

- A listas ordenadas e não ordenadas podem ter outro desenho a frente, será ensinado mais a frente quando construirmos layouts.

<h4 style="color: red;">Tabela</h4>

{% highlight html %}
<table border="1">
  <tr>
    <th>Cabeçalho 1</th>
    <th>Cabeçalho 2</th>
    <th>Cabeçalho 3</th>
  </tr>
  <tr>
    <td>Linha 1 - Célula 1</td>
    <td>Linha 1 - Célula 2</td>
    <td>Linha 1 - Célula 3</td>
  <tr>
  <tr>
    <td>Linha 2 - Célula 1</td>
    <td>Linha 2 - Célula 2</td>
    <td>Linha 2 - Célula 3</td>
  <tr>
</table>
{% endhighlight %}

- Na tabela colocamos o atributo <b>border="1"</b>, ele define que a tabela terá bordas de tamanho 1.

<h4 style="color: red;">DIV</h4>

{% highlight html %}
<h4>Está é uma lista ordenada</h4>
<div></div>
{% endhighlight %}

- A tag <b>div</b> é um container de conteúdo, sozinha ela não faz nada, mas será muito utilizada para a estrutura das páginas.

Documento completo
{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>Aula Um</title>
  </head>
  <body>
    <h1>Eu sou um título tamanho H1</h1>
    <h2>Eu sou um sub-título tamanho H2</h2>
    <h3>Eu sou um sub-título tamanho H3</h3>
    <h4>Eu sou um sub-título tamanho H4</h4>
    <h5>Eu sou um sub-título tamanho H5</h5>
    <h6>Eu sou um sub-título tamanho H6</h6>

    <p>Eu sou um paragrafo.</p>
    <p>Eu sou outro paragrafo.</p>

    <a href="https://programadoresreais.com.br/">Eu sou um link</a>

    <br>

    <button>Eu sou um botão</button>

    <h4>Abaixo uma lista não ordenada</h4>
    <ul>
      <li>Aula 1</li>
      <li>Aula 2</li>
      <li>Aula 3</li>
    </ul>

    <h4>Está é uma lista ordenada</h4>
    <ol>
      <li>Aula 1</li>
      <li>Aula 2</li>
      <li>Aula 3</li>
    </ol>

    <table border="1">
      <tr>
        <th>Cabeçalho 1</th>
        <th>Cabeçalho 2</th>
        <th>Cabeçalho 3</th>
      </tr>
      <tr>
        <td>Linha 1 - Célula 1</td>
        <td>Linha 1 - Célula 2</td>
        <td>Linha 1 - Célula 3</td>
      <tr>
      <tr>
        <td>Linha 2 - Célula 1</td>
        <td>Linha 2 - Célula 2</td>
        <td>Linha 2 - Célula 3</td>
      <tr>
    </table>

    <div></div>
  </body>
</html>
{% endhighlight %}


Encerramos por aqui o conceito e algumas tags básicas do HTML, siga o blog que será ensinado a construção completa de um site.

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/carreira-full-stack.html">Carreira Full Stack</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/front-end/css/css-parte-um-conceitos-basicos.html">CSS - Parte I - Conceitos básicos</a></div>

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
