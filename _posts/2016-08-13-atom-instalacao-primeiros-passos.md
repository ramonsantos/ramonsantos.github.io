---
layout: post
title: "Atom: instalação e primeiros passos"
date: 2016-08-13 14:27:19 -0300
categories: 'Ferramentas'
tags:
  - Atom
  - Desenvolvimento Web
  - IDE
description: Instalação e introdução ao editor Atom.
---

<div style="text-align: center; display:none">
  <img src="/images/atom-instalacao-primeiros-passos/atom-icon.png" style="max-width: 100%" alt="Atom" />
</div>

Sempre houve, e haverá, aquela discussão sobre qual IDE/Editor é o melhor. Eu acredito que a resposta para isso vai do gosto de cada um. Felizmente, hoje existe uma boa variedade de editores de texto para desenvolvimento. Entre os mais populares estão: [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), [Brackets](http://brackets.io/), [Gedit](https://wiki.gnome.org/Apps/Gedit), [Notepad++](https://notepad-plus-plus.org/), [Emacs](https://www.gnu.org/software/emacs/), [Geany](https://www.geany.org/), [Vim](http://www.vim.org/), [Textmate](https://macromates.com/) e [Visual Studio Code](https://code.visualstudio.com/). Atualmente o meu editor preferido é o <strong>Atom</strong>.

O Atom é um editor de texto open source indicado para desenvolvedores. Foi inicialmente desenvolvido pelo <strong>GitHub</strong> e seu repositório oficial [está disponível no próprio Github](https://github.com/atom/atom).

## Instalação

Uma das características deste editor é que ele é multiplataforma. Para **Linux**, o Atom é <a href="https://atom.io/" title="Site oficial do Atom" target="_blank">disponibilizado</a> em pacotes *.deb* e *.rpm*, além da possibilidade de instalação a partir dos fontes e contando com um excelente <a href="https://github.com/atom/atom/blob/master/docs/build-instructions/linux.md" target="_blank">tutorial</a>.

Com o pacote de sua distribuição baixado, basta entrar no diretório onde o mesmo se encontra e executar um dos comando abaixo de acordo com sua distro.

#### Família Debian (Debian, Ubuntu, Linux Mint e etc):

<pre class="terminal">
  $ sudo dpkg -i atom-amd64.deb
</pre>

#### Família Red Hat (Fedora, CentOS, openSUSE e etc):

<pre class="terminal">
  $ sudo rpm -Uvh atom.x86_64.rpm
</pre>

## Recursos nativos

Por padrão, o Atom já vem como vários recursos uteis, entre eles temos:

  * *Integração com o Github*;
  * *Gerenciador de pacotes*;
  * *Syntax highlight*;
  * *Live preview para arquivos Markdown*;
  * *Divisão de Painéis (Split)*;
  * *Tree view para diretórios e arquivos*.

<div style="text-align: center"><a href="/images/atom-instalacao-primeiros-passos/atom-live-preview-md.png" target="_blank"><figure><img src="/images/atom-instalacao-primeiros-passos/atom-live-preview-md.png" style="max-width: 100%" alt="Live Preview para Markdown" title="Live Preview para Markdown" /><figcaption class="text-center">Live Preview para Markdown.</figcaption></figure></a></div>

<div style="text-align: center"><a href="/images/atom-instalacao-primeiros-passos/atom-split.png" target="_blank"><figure><img src="/images/atom-instalacao-primeiros-passos/atom-split.png" style="max-width: 100%" alt="Divisões de Painéis (Split)" title="Divisões de Painéis (Split)" /><figcaption class="text-center">Divisões de Painéis (Split).</figcaption></figure></a></div>

## Personalizando o Atom

Agora vamos para a melhor parte, os pacote. Como mencionado acima, o gerenciador do pacotes já vem ativado por padrão, para acessá-lo entre no menu <em>Edit</em> > <em>Preferences</em>, vai aparecer a aba "<em>Settings</em>".

Na aba "Settings" podemos definir teclas de atalhos (Keybindings), configuração gerais (Settings), instalar (install) e atualizar (updates) pacotes e temas, gerenciar pacotes instalados (Packages) e escolher o visual da aplicação (Themes).

Para ilustrar o potencial de personalização do atom, vamos deixá-lo parecido com o <strong>Sublime Text</strong>. Duas características são icônicas no Sublime Text: o tema "<strong>monokai</strong>" e o "<strong>minimap</strong>".

### Instalando um tema

Para instalar o tema vá em "<em>Install</em>", digite "<em>monokai</em>" e click em "<em>Themes</em>". Entre as opções escolha "<em>monokai</em>" do usuário "<em>kevinsawicki</em>" e click em "<em>Install</em>".

Depois de instalação, vá em "<em>Themes</em>" para configurar o tema. Em "<em>UI Theme</em>" escolha "<em>Atom Light</em>" e em "<em>Syntax Theme</em>" escolha "<em>Monokai</em>".

### Instalando um pacote

Para instalar um pacote o procedimento é similar, vá em "<em>Install</em>", digite "<em>minimap</em>" e precione "<em>enter</em>" ou click em "<em>Packages</em>". Escolha o pacote "<em>minimap</em>" do usuário "<em>atom-minimap</em>" e click em "<em>Install</em>".

Geralmente os pacotes são ativados logo após serem instalados, para conferir vá em "<em>Packages</em>" e veja se o pacote está ativo, caso não esteja click em "<em>Enable</em>".

A aparencia do Atom ficará como na figura abaixo.

<div style="text-align: center"><a href="/images/atom-instalacao-primeiros-passos/atom-monokai-theme.png" target="_blank"><figure><img src="/images/atom-instalacao-primeiros-passos/atom-monokai-theme.png" style="max-width: 100%" alt="Visual do Atom depois da personalização" title="Visual do Atom depois da personalização" /><figcaption class="text-center">Visual do Atom depois da personalização.</figcaption></figure></a>
</div>

Por enquanto é isso. Em breve vou mostrar outras características do Atom.

<br>
Abraços!
