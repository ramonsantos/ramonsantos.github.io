---
layout: post
title: Como instalar o Gnuplot no Fedora
date: 2016-08-06 14:42:50 -0300
tags:
  - Fedora
  - Ferramentas Acadêmicas
categories: Ferramentas
description: Instalação do Gnuplot no fedora.
permalink: "blog/como-instalar-gnuplot-fedora/"
---

Olá, pessoal!

Hoje vamos ver como instalar o **Gnuplot** no **Fedora**. Para quem não conhece, [Gnuplot](http://www.gnuplot.info/) é uma ferramenta muito usada no meio acadêmico para plotar gráficos de funções matemáticas em 2D e 3D, sendo que a saída pode ser apresentada diretamente na tela ou exportada para arquivos em diversos formatos, como *PNG*, *JPEG*, *SVG* e *EPS*.

O Gnuplot não é disponibilizado por padrão nos repositórios oficiais do Fedora, desta forma, é necessário [fazer o download do software manualmente](https://sourceforge.net/projects/gnuplot/files/gnuplot/).

Depois de fazer o download devemos abrir o terminal, entrar no diretório onde está o arquivo e descompactá-lo. Supondo que o nome do arquivo é <em>"gnuplot-5.0.3.tar.gz"</em> e está em <em>"/home/user/Downloads"</em>, entre com os comandos abaixo no terminal.

Entrar no diretório do download:

<pre class="terminal">
  $ cd Downloads
</pre>

<p>Descompactar o arquivo de instalação:</p>

<pre class="terminal">
  $ tar -vzxf gnuplot-5.0.3.tar.gz
</pre>

<p>Entrar no diretório descompactado:</p>

<pre class="terminal">
  $ cd gnuplot-5.0.3
</pre>

Agora vamos para a instalação propriamente dita. Entre com os comandos abaixo:

<pre class="terminal">
  $ ./configure
</pre>

<pre class="terminal">
  $ sudo make install
</pre>

Se não houver problemas durante esse processo, a instalação será concluída com sucesso. Para verificar se o software está funcionando, vamos fazer uma espécie de <em>"Hello Word"</em>, ou seja, vamos plotar uma gráfico simples.

Para entrar no Gnuplot vá ao terminal e faça:

<pre class="terminal">
  $ gnuplot
</pre>

Com o Gnuplot aberto no terminal, vamos plotar o gráfico de sen(x):

<pre class="terminal">
  gnuplot> plot sin(x)
</pre>

Com isso, uma janela deverá ser aberta com o gráfico da função como na figura abaixo.

<div style="text-align: center"><a href="/images/como-instalar-gnuplot-fedora/gnuplot-sin-x.png" target="_blank"><figure><img src="/images/como-instalar-gnuplot-fedora/gnuplot-sin-x.png" style="max-width: 100%" alt="Imagem plotada através do Gnuplot" title="Imagem plotada através do Gnuplot" /><figcaption class="text-center">Imagem plotada através do Gnuplot.</figcaption></figure></a>
</div>

Fácil, não é? Eu usei o Gnuplot para gerar os gráficos do [meu TCC](http://www.slideshare.net/RamonSantos28/tcc-avaliao-de-dependabilidade-e-anlise-de-sensibilidade-de-uma-plataforma-como-servio-paas) e a qualidade ficou muito boa. Para finalizar, uma outra dica é exportar os gráficos gerados para formatos vetoriais, como o **EPS** ou o **SVG**.

<br/>
<p>Abraços!</p>
