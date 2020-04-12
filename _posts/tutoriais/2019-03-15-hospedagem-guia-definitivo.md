---
layout: post
title:  "Hospedagem - Guia definitivo"
date:   2019-03-14 10:36:53 -0200
categories: tutoriais
permalink: /:categories/:title.html
author: "Lucas"
description: "Passo a passo de como hospedar sites de forma grátis e paga e usando filezilla"
---

Quando iniciamos no desenvolvimento e conseguimos fazer o primeiro site, aqueles bem simples, queremos mostrar ao mundo o resultado de nossos esforços e dedicação nos estudos, e nesse momento nos deparamos com a hospedagem de sites.

As duvidas são imensas e muitas pessoas se esbarram nesse ponto, então aqui está um "Guia definitivo sobre hospedagem de sites".

Imagino que se você está aqui é porque já tem um site pronto, mas caso não tenha estou deixando o link de um projeto de site portfólio no GitHub para download e uso no processo de hospedagem.

[GitHub - Portfólio](https://github.com/luhcasJL/blog/tree/master/portfolio)

Então vamos ao tutorial.

Para, para, para ...

Primeiro vamos aos requisitos.

Vamos precisar ter instalado no computador o [FileZilla](https://filezilla-project.org/), ele serve para conectar com a hospedagem para podermos enviar arquivos de maneira fácil e rápida para o servidor.

Vou dividindo o tutorial entre uma hospedagem gratuita e uma paga.

Algumas empresas que fornecem hospedagem gratuita:

- [000webhost](https://br.000webhost.com/)
- [freehostia](https://www.freehostia.com/)
- [awardspace](https://www.awardspace.com/)

Usarei o último da lista, faça o cadastro no site, eu tentei fazer pelo primeiro, mas sério, experiência horrível.

Depois de verificar o registro e entrar acessar a hospedagem vai se deparar com o cpanel (painel de controle),

<img src="/assets/imagens/hospedagem/cpanel.JPG"/>

se você estiver usando uma hospedagem paga terá um cpanel mais ou menos assim

<img src="/assets/imagens/hospedagem/cpanel_hostgator.png"/>

Esse trecho somente para quem está fazendo pela hospedagem do "awardspace", se você usa uma hospedagem paga, possivelmente já tem domínio contratado e configurado na contratação hospedagem.
Caso não tenha recomendo sempre comprar direto no [Registro BR](https://registro.br/), sério, eles não aumentam o valor na renovação. Neste caso terá que configurar o dns, caso não saiba como fazer deixe nos comentários pedindo que eu faço um artigo sobre.

{% highlight html %}
Agora precisaremos de um domínio (endereço do site), siga os passos:
- entre em "Gerenciador de domínios",
- vai em "Registrar um Domínio Grátis"
- escolha um nome de domínio
- clique em registar e vai prosseguindo sem adicionar nenhum produto a mais
- preenche o seu endereço
- concorde com os termos e diga que não é um robo
- tenha seu domínio e seja feliz ^.^
{% endhighlight %}

Fim do trecho.

A partir de agora precisaremos do acesso ftp da hospedagem.

- entre em "Gerenciador FTP",
- caso esteja em um pago procure por "Contas de FTP", escolha a conta que de acesso ao public_ftp
- clique no ícone de configure ftp
<img src="/assets/imagens/hospedagem/ftp.JPG"/>
- Arquivos de configuração do FTP
- Baixa o arquivo FileZilla
<img src="/assets/imagens/hospedagem/filezilla.JPG"/>

Finalmente vamos hospedar

- Abra o FileZilla
- Vá em arquivo
- Vá em importar
- Selecione o arquivo que você baixou e faça a importação
- Clique aqui

<img src="/assets/imagens/hospedagem/f1.JPG"/>

- Selecione a hospedagem

<img src="/assets/imagens/hospedagem/f2.JPG"/>

- No tipo de logon mude para normal
- coloque a senha de acesso ao site de hospedagem
- Não mude mais nada
- Clique em conectar
- Quando perguntar, marque a opção confiar nesse certificado nas sessões futuras

Voa-lá, estamos com acesso ao servidor de hospedagem,

Entre na pasta com o nome do seu site,

<img src="/assets/imagens/hospedagem/f5.JPG"/>

Se estiver em uma hospedagem paga entre na pasta "public_html", apague o que tiver dentro dela

Agora vá na pasta que estão os arquivos do site a ser hospedado

<img src="/assets/imagens/hospedagem/f3.JPG"/>

Selecione todos os arquivos e solte aqui

<img src="/assets/imagens/hospedagem/f4.JPG"/>

Terminado o processo entre em seu site.

O meu é [http://tutorialhospedagem.dx.am/](http://tutorialhospedagem.dx.am/)

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

<div style="display: inline;">Anterior: <a href="https://programadoresreais.com.br/conceitos/mvc-uma-breve-explicacao.html">MVC - Uma breve explicação</a></div><div style="float: right">Próximo: <a href="https://programadoresreais.com.br/carreira-full-stack.html">Carreira Full Stack</a></div>

<br><br>
Planejamento de artigos:
- CodeIgniter - Primeiro projeto
- Projeto e-commerce - desenvolvimento completo dividido em artigos
- CPanel - Guia definitivo

<br><br>
Comentem aqui em baixo, tirem dúvidas, e esperem pelo novo artigo.

Tem um sugestão de artigo? Deixe nos comentários.

Gostou do meu serviço? Me contrate chamando pelo wpp ou mande um e-mail.
<br><br>

{% include disqus.html %}
