---
layout: post
title:  "MVC - Uma breve explicação"
date:   2019-03-14 10:36:53 -0200
categories: conceitos
permalink: /:categories/:title.html
author: "Lucas"
description: "Arquitetura de software usando Model, View e Controller"
---

Hoje eu vou explicar como desenvolver os projetos em arquitetura MVC.

MVC é um padrão de arquitetura de software que divide o projeto em Model, View e Controller.

A arquitetura fica assim.

<img src="/assets/imagens/mvc/arquitetura.JPG" style="float: left; margin-right: 5%;"/>

<h4 style="color: #FF0000;">View</h4>

A view é onde desenvolvemos o código visual e de interação com os usuários. Aqui é onde vai todo o HTML, aqui é extremamente proibido códigos sql.

Os arquivos da View começam em minúsculo, exemplo.php

<br>
<h4 style="color: #FF0000;">Controller</h4>

A controller fica responsável por fazer todo o controle do sistema. Ele recebe as requisições, define qual informação a model chamará do banco de dados, aqui fazemos o controle de acesso entre muitas outras coisas.

Os arquivos da Controller começam em maiúsculo, Exemplo.php

<h4 style="color: #FF0000;">Model</h4>

Por fim sobrou a model, ela fica responsável por fazer todas as requisições ao banco de dados e retornar o resultado a controller, todas as querys sql estão aqui.

Os arquivos da Model começam em maiúsculo e são acompanhadas com "_model", Exemplo_model.php

<h4 style="color: #FF0000;">Mas por que eu faria assim? Eu já sei fazer muito bem no modelo estruturado</h4>

Ok, temos essa dúvida frequentemente quando estamos iniciando nos estudos de desenvolvimento. Vamos a algumas vantagens da arquitetura MVC.

A grande vantagem em desenvolver utilizando MVC fica na agilidade de desenvolvimento, facilidade na manutenção, código super limpo e rápido.

Quando pegamos códigos de programadores iniciantes nos deparamos com uma quantidade imensa de arquivos. Para cada requisição SQL tem um arquivo separado.

<h4>Estruturado</h4>
<img src="/assets/imagens/mvc/estruturado.JPG" style="float: left; margin-right: 5%;"/>

Perceba que neste exemplo que todos os arquivos estão misturados, não dá nem pra saber qual arquivo está o HTML. Imagine um projeto com mais 50 destas pastas a dificuldade de se achar o arquivo que está com a requisição de algo.

É de se imaginar que isso é considerado trabalho de amador e que sem código limpo e saudável nada de ótimos salários.

<div style="clear: both;"></div>
<br>
<h4>Arquitetura em MVC</h4>
<img src="/assets/imagens/mvc/mvc.JPG" style="float: left; margin-right: 5%;"/>
Note que neste criamos uma área na view para clientes e nele colocamos todos os arquivos de interação, uma página com a lista de todos os clientes, uma página que mostra o detalhe do cliente e por fim uma página que faz o cadastro do cliente.

"Aaah, mas eu já separo as views por arquivo."

Calma meu bom rapaz ou moça, perceba que só temos 1 controller para cuidar de toda a parte lógica da área clientes, e isso faz uma economia de horas quando se precisa fazer manutenção.

E uma vantagem muito importante também é que diminui de forma espantosa a quantidade de erros nas aplicações, quem já não se deparou, leu ou ouviu em algum lugar que no projeto surgia mais erros do que se podiam arrumar?

<h4 style="color: #FF0000;">Frameworks PHP em arquitetura MVC</h4>

- CakePHP
- CodeIgniter
- Laravel
- Zend Framework

Eu utilizo atualmente o CodeIgniter e ensinarei a utiliza-lo neste blog.

Este foi um artigo rápido com o conceito de arquitetura MVC, espero que tenham gostado.

Texto revisado em 15/03/2019, encontrou algum erro de português? Deixe nos comentários, será bastante útil.

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

<div style="display: inline;">Anterior: <a href="http://lucasalves.ml/templates/primeiro-layout.html">Primeiro layout</a></div><div style="float: right">Próximo: <a href="http://lucasalves.ml/tutoriais/hospedagem-guia-definitivo.html">Hospedagem - Guia definitivo</a></div>

<br><br>
Planejamento de artigos:
- MVC - Mão na massa
- CodeIgniter - Primeiro projeto
- Projeto e-commerce - desenvolvimento completo dividido em artigos
<br><br>

Comentem aqui em baixo, tirem dúvidas, de sugestão, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>
{% include disqus.html %}
