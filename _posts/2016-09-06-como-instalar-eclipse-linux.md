---
layout: post
title: Como instalar o Eclipse no Linux
date: 2016-09-06 21:54:37 -0300
categories: 'Ferramentas'
tags:
  - Desenvolvimento Web
  - Eclipse
  - IDE
description:
---

<div style="text-align: center; display:none">
  <img src="/images/como-instalar-eclipse-linux/eclipse.png" style="max-width: 100%" alt="Eclipse Linux" />
</div>

O <strong>[Eclipse](https://eclipse.org/)</strong> é uma excelente ferramenta, [open source](https://github.com/eclipse), para desenvolvimento de aplicações em <strong>Java</strong> e em outras linguagens. Neste artigo, será abordado a instalação desta ferramenta em sistemas <strong>Linux</strong>. O único pré-requisito para ter o Eclipse em sua máquina, é ter o [JDK instalado](https://ramonsantos.github.io/blog/como-instalar-java-fedora/).

A primeira coisa a ser feita é o [download do Eclipse](https://eclipse.org/downloads/), sendo que a versão mais recente é o [Eclipse Neon](https://projects.eclipse.org/releases/neon).

Dado que o dowload foi feito no diretório <em>"/home/user/Downloads"</em>, execute no terminal:

<pre class="terminal">
  $ cd Downloads
  $ tar -vzxf eclipse*
  $ sudo chmod 777 /opt
  $ sudo mv eclipse /opt
</pre>

Feito isso, agora vamos criar uma entrada de desktop (atalho) para o Eclipse. No terminal faça:

<pre class="terminal">
  $ cd /usr/share/applications
  $ sudo gedit eclipse.desktop
</pre>

Uma janela do gedit será aberta, entre com o conteúdo a seguir, salve o arquivo e feche o editor.

<script src="https://gist.github.com/ramonsantos/a032f9938705be19b42ee8f3c334614b.js"></script>

Por fim, vamos criar um link simbólico.

<pre class="terminal">
  $ cd /usr/local/bin
  $ sudo ln -s /opt/eclipse/eclipse
</pre>

Se tudo ocorreu bem, basta acessar o Eclipse através do ícone no lançador de seu ambiente gráfico, no meu caso é o gnome, ou pelo terminal:

<pre class="terminal">
  $ eclipse
</pre>

Está Feito! Este artigo foi sucinto pois, como vocês devem ter percebido, a instalação do Eclipse é bastante simples. Originalmente eu fiz esse tutorial para o Ubuntu ainda durante minha graduação, quando eu era monitor da cadeira de Programação Orientada a Objetos (POO) e "forçava" meus colegas a usarem Linux. Além do <strong>Ubuntu</strong> e do <strong>Fedora</strong>, o procedimento usado neste post servirá para qualquer distribuição Linux de Desktops.

<br>
Abraços!
