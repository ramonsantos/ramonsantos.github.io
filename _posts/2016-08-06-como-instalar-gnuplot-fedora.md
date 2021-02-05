---
layout: post
title: Como instalar o Gnuplot no Fedora
date: 2016-08-06 14:42:50 -0300
categories: Ferramentas
tags:
  - Fedora
  - Ferramentas Acadêmicas
  - Linux
description: Instalação do Gnuplot no fedora.
image:
  path: "/images/como-instalar-gnuplot-fedora/gnuplot-sin-x.png"
---

Vamos ver como instalar o **Gnuplot** no **Fedora**. Para quem não conhece, [Gnuplot](http://www.gnuplot.info/) é uma ferramenta muito usada no meio acadêmico para plotar gráficos de funções matemáticas em 2D e 3D, sendo que a saída pode ser apresentada diretamente na tela ou exportada para arquivos em diversos formatos, como *PNG*, *JPEG*, *SVG* e *EPS*.

O Gnuplot não é disponibilizado por padrão nos repositórios oficiais do Fedora, desta forma, é necessário [fazer o download do software manualmente](https://sourceforge.net/projects/gnuplot/files/gnuplot/).

Depois de fazer o download devemos abrir o terminal, entrar no diretório onde está o arquivo e descompactá-lo. Supondo que o nome do arquivo é ```gnuplot-5.0.3.tar.gz``` e está em ```/home/user/Downloads```, entre com os comandos abaixo no terminal.

Entrar no diretório do download:

<pre><code class="shell terminal">
$ cd Downloads
</code></pre>

<p>Descompactar o arquivo de instalação:</p>

<pre><code class="shell terminal">
$ tar -vzxf gnuplot-5.0.3.tar.gz
</code></pre>

<p>Entrar no diretório descompactado:</p>

<pre><code class="shell terminal">
$ cd gnuplot-5.0.3
</code></pre>

Agora vamos para a instalação propriamente dita. Entre com os comandos abaixo:

<pre><code class="shell terminal">
$ ./configure
</code></pre>

<pre><code class="shell terminal">
$ sudo make install
</code></pre>

Se não houver problemas durante esse processo, a instalação será concluída com sucesso. Para verificar se o software está funcionando, vamos fazer uma espécie de *Hello Word*, ou seja, vamos plotar uma gráfico simples.

Para entrar no Gnuplot vá ao terminal e faça:

<pre><code class="shell terminal">
$ gnuplot
</code></pre>

Com o Gnuplot aberto no terminal, vamos plotar o gráfico de *sen(x)*:

<pre><code class="shell terminal">
gnuplot> plot sin(x)
</code></pre>

Com isso, uma janela deverá ser aberta com o gráfico da função como na figura abaixo.

<div style="text-align: center"><a href="/images/como-instalar-gnuplot-fedora/gnuplot-sin-x.png" target="_blank"><figure><img src="/images/como-instalar-gnuplot-fedora/gnuplot-sin-x.png" style="max-width: 100%" alt="Imagem plotada através do Gnuplot" title="Imagem plotada através do Gnuplot" /><figcaption class="text-center">Imagem plotada através do Gnuplot.</figcaption></figure></a>
</div>

Eu usei o Gnuplot para gerar os gráficos do [meu TCC](http://www.slideshare.net/RamonSantos28/tcc-avaliao-de-dependabilidade-e-anlise-de-sensibilidade-de-uma-plataforma-como-servio-paas) e a qualidade ficou muito boa. Para finalizar, uma outra dica é exportar os gráficos gerados para formatos vetoriais, como o **EPS** ou o **SVG**.
