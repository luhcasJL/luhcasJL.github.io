---
layout: post
title:  "MySQL - A importância de identificar corretamente"
date:   2020-04-12 15:36:53 -0200
categories: conceitos
permalink: /:categories/:title.html
author: "Lucas"
description: "Chaves primarias estrangeiras de forma consciente"
---

Boas devs,

Esta semana me deparei com um problema sutil na concepção de um banco de dados usando o MySQL e que se tornou uma grande dor de cabeça.

Antes de falar sobre o problema, vamos a alguns conceitos básicos.

<h4 style="color: #FF0000;">MySQL</h4>

O MySQL é um sistema de gerenciamento de banco de dados, que utiliza a linguagem SQL como interface. É atualmente um dos sistemas de gerenciamento de bancos de dados mais populares da Oracle Corporation, com mais de 10 milhões de instalações pelo mundo. (<a href="https://pt.wikipedia.org/wiki/MySQL" target="_blank"> Wikipédia </a>)

<h4 style="color: #FF0000;">SQL</h4>

Structured Query Language, ou Linguagem de Consulta Estruturada ou SQL, é a linguagem de pesquisa declarativa padrão para banco de dados relacional. Muitas das características originais do SQL foram inspiradas na álgebra relacional. (<a href="https://pt.wikipedia.org/wiki/SQL" target="_blank"> Wikipédia </a>)

<h4 style="color: #FF0000;">Primary Key</h4>

A primary key (chave primária) é o principal identificador de um registro, ela não se repete, aconselhável ser um número inteiro sequencial.

<h4 style="color: #FF0000;">Foreign Key</h4>

A foreign key (chave estrangeiro) serve para relacionar 2 tabelas, sempre que temos 1 tabela que precisa usar dados de outra tabela usamos uma foreign key.

<h4 style="color: #FF0000;">Unique</h4>

Não é porque um dado não deve se repetir que ele será uma primary key, é o caso do CPF, sempre que ele não deva ser repetido, deverá ser definido como único na tabela.

<h4 style="color: #FF0000;">Caso prático 1</h4>

Tiremos como exemplo um prédio:
 - Criamos primeiramente o banco de dados de nome predio.

 - O principal elemento que um prédio tem são apartamentos, sendo assim criamos no banco de dados uma tabela chamada apartamentos, para ficar simples ela só terá os campos id e número do apartamento.

 <div style="text-align: center;">
   <img src="/assets/imagens/conceitos/banco_dados/table_apartamentos.PNG"/>
 </div>

 O id do apartamento foi definido com a primary key e com auto increment.

 - Já o apartamento tem moradores, criamos também a tabela correspondente.

 <div style="text-align: center;">
   <img src="/assets/imagens/conceitos/banco_dados/table_no_moradares.PNG"/>
 </div>

O id do apartamento foi definido com a primary key e com auto increment e o CPF foi definido como unique, já que uma mesma pessoa não pode ser registrada duas vezes como moradora do prédio.

<h4 style="color: #FF0000;">Mas afinal, como funcionam os relacionamentos?</h4>

Analisando o caso do prédio, percebemos que temos duas tabelas mas que não tem nenhum campo que defina em que um apartamento se relacione com moradores ou vice-versa.

Isso é resolvido incluindo uma foreign key na tabela moradores.

<div style="text-align: center;">
  <img src="/assets/imagens/conceitos/banco_dados/table_yes_moradares.PNG"/>
</div>

Desta forma temos como relacionar as duas tabelas.

<h4 style="color: #FF0000;">Caso prático 2</h4>

Agora imagine que estamos fazendo um pequeno controle de para um mercadinho do seu bairro.

Vamos analisar apenas os dados do produto, entradas de estoque e alterações de preço do produto.

Sendo assim teremos 3 tabelas, sendo a principal a tabela produtos.

<div style="text-align: center;">
  <img src="/assets/imagens/conceitos/banco_dados/table_produtos.PNG"/>
</div>

O EAN é o código de barras do produto e jamais devemos coloca-lo como chave estrangeira, assim:

<div style="text-align: center;">
  <img src="/assets/imagens/conceitos/banco_dados/table_historico_no_preco.PNG"/>
</div>

Agora vou dizer porque você não deve relacionar assim, imagine que seja um supermercado grande, que tenha milhares de produtos, que os preços são alterados frequentemente, e que um produto X tenha sido cadastrado no dia 10/01/2002 e que no dia 15/01/2020 um funcionário percebeu que o código ean foi cadastrado incorretamente e que já se tenha realizado centenas de vendas, alterações de preço e entradas de estoque;

Ou pior que apesar de o back-end ter feito validações para um produto não se repetir, o EAN na tabela produtos não estava como UNIQUE e o funcionário conseguiu cadastrar um produto 2 vezes, e se alterar os dados do novo produto ele altera os dados dos dois registros, e vamos piorar o cenário, que o código errado seja um código válido de um produto cadastrado a 6 meses atrás, parece impossível ou improvável, pois é jovem padawan, se isto acontecer, o caos está instalado neste mercado e na empresa de tecnologia que mantém este sistema.

Foi isto que aconteceu a semana passada em um ERP, com a grande sorte de ter sido percebido 2 minutos após o cadastro do novo produto, e motivo deste artigo estar sendo escrito.

Pois bem, faça a tabela desta forma.

<div style="text-align: center;">
  <img src="/assets/imagens/conceitos/banco_dados/table_produtos_yes.PNG"/>
</div>
Defina o código EAN como UNIQUE.

<div style="text-align: center;">
  <img src="/assets/imagens/conceitos/banco_dados/table_historico_yes_preco.PNG"/>
</div>
Faça com que a chave estrangeira seja o id do produto.

Este artigo termina por aqui, escreverei um artigo falando sobre o problema e como ele foi resolvido. Ah, o blog tem um grupo no WhatsApp, entra lá.
<a href="https://chat.whatsapp.com/KHya5ibxrqY8dS2fmdBSjM" target="_blank">Grupo WPP</a>

<br>
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

<br><br>
Comentem aqui em baixo, marquem gostei, tirem dúvidas, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>

{% include disqus.html %}
