---
layout: post
title: Como criar chave SSH no Linux
date: 2016-10-29 20:35:49 -0300
categories: 'Linux'
permalink: '/blog/como-criar-chave-ssh-linux/'
tags:
  - Git
  - Github
  - Deploy
description:
---

Olá, pessoal!

Hoje eu vou mostrar como gerar uma chave SSH (SSH key).

A primeira coisa a fazer é verificar se já existe uma chave SSH no sistema. Em geral, essas chaves ficam do diretório oculto “/home/USER/.ssh”, então execute o comando abaixo:

<pre class="terminal">
  $ ls ~/.ssh
</pre>

Dado que o esse diretório está vazio, podemos gerar a chave com o seguinte comando:

<pre class="terminal">
  $ ssh-keygen -t rsa -b 4096 -C "seu.email@dominio.com"
</pre>

Quanto a mensagem abaixo for exibida no terminal, pressione a tecla “Enter” para deixar a chave no diretório padrão.

<pre class="terminal">
    Enter a file in which to save the key (/Users/you/.ssh/id_rsa):
</pre>

Logo depois será requisitado uma “passphrase”.

<pre class="terminal">
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
</pre>

O processo será concluído e no terminal irá aparecer algo parecido com isso:

<pre class="terminal">
    SHA256: kjerwerJGwfwef515151IGUYFIvjhbbyudwu456yfbJ seu.email@dominio.com
    The key's randomart image is:
    +---[RSA 4096]----+
    |       +*..+*    |
    |      =. +.=     |
    |     . . .o .    |
    |         o+   E  |
    |        S= . + o |
    |        . o o +  |
    |           .   . |
    |                 |
    |                 |
    +----[SHA256]-----+
</pre>

<br>
Abraços!
