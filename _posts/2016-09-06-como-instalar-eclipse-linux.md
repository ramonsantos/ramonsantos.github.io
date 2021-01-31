---
layout: post
title: Como instalar o Eclipse no Linux
date: 2016-09-06 21:54:37 -0300
categories: 'Ferramentas'
tags:
  - Ferramentas de Desenvolvimento
  - Java
description:
image:
  path: "/images/como-instalar-eclipse-linux/eclipse.png"
---

O <strong>[Eclipse](https://eclipse.org/)</strong> é uma excelente ferramenta, [open source](https://github.com/eclipse), para desenvolvimento de aplicações em <strong>Java</strong> e em outras linguagens. Neste artigo, será abordado a instalação desta ferramenta em sistemas <strong>Linux</strong>. O único pré-requisito para ter o Eclipse em sua máquina, é ter o [JDK instalado](https://ramonsantos.github.io/blog/como-instalar-java-fedora/).

A primeira coisa a ser feita é o [download do Eclipse](https://eclipse.org/downloads/), sendo que a versão mais recente é o [Eclipse Neon](https://projects.eclipse.org/releases/neon).

Dado que o dowload foi feito no diretório <em>"/home/user/Downloads"</em>, execute no terminal:

<pre><code class="shell terminal">
$ cd Downloads
$ tar -vzxf eclipse*
$ sudo chmod 777 /opt
$ sudo mv eclipse /opt
</code></pre>

Feito isso, agora vamos criar uma entrada de desktop (atalho) para o Eclipse. No terminal faça:

<pre><code class="shell terminal">
$ cd /usr/share/applications
$ sudo gedit eclipse.desktop
</code></pre>

Uma janela do gedit será aberta, entre com o conteúdo a seguir, salve o arquivo e feche o editor.

<pre><code class="plaintext">
[Desktop Entry]
Name=Eclipse
Type=Application
Exec=/opt/eclipse/eclipse
Terminal=false
Icon=/opt/eclipse/icon.xpm
Comment=Integrated Development Environment
NoDisplay=false
Categories=Development;IDE
Name[en]=Eclipse
</code></pre>

Por fim, vamos criar um link simbólico.

<pre><code class="shell terminal">
$ cd /usr/local/bin
$ sudo ln -s /opt/eclipse/eclipse
</code></pre>

Se tudo ocorreu bem, basta acessar o Eclipse através do ícone no lançador de seu ambiente gráfico, no meu caso é o gnome, ou pelo terminal:

<pre><code class="shell terminal">
$ eclipse
</code></pre>
