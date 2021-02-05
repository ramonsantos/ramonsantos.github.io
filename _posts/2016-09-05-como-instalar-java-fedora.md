---
layout: post
title: Como instalar o Java no Fedora
date: 2016-09-05 19:10:58 -0300
categories: Ferramentas
tags:
  - Fedora
  - Java
  - Linux
description:
image:
  path: "/images/como-instalar-java-fedora/java.png"
---

O objetivo deste post é mostrar **como instalar o JDK no Fedora**, no entanto, este artigo pode servir para outras distribuições da família **Red Hat**, como é o caso de **[CentOS](https://www.centos.org/)**.

Primeiramente é preciso fazer o [download do pacote RPM do JDK através do site oficial](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). A versão mais atual do JDK neste momento é a ```1.8.101```. Desta forma, escolha o pacote referente à arquitetura de sua máquina (32 bits ou 64 bits).

Supondo que o download do pacote de instalação foi feito no o diretório ```/home/user/Downloads``` e o arquivo chama-se ```jdk-8u101-linux-x64.rpm```, entre com os seguintes comandos no terminal:

<pre><code class="shell terminal">
$ cd Downloads
$ sudo rpm -Uvh jdk-8u101-linux-x64.rpm
$ sudo alternatives --install /usr/bin/java java /usr/java/latest/jre/bin/java 200000
</code></pre>

Após a instalação é importante definir qual a versão padrão do **JDK** no sistema operacional, dado que o **Fedora** já vem com o **[OpenJDK](http://openjdk.java.net/)** instalado. Para isso, entre com o comando abaixo no terminal:

<pre><code class="shell terminal">
$ sudo alternatives --config java

  Há 3 programas que oferecem "java".

  Seleção    Comando
  -----------------------------------------------
  *  1           java-1.8.0-openjdk.x86_64 (/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.101-1.b14.fc24.x86_64/jre/bin/java)
  +  2           /usr/java/jdk1.8.0_101/jre/bin/java
     3           /usr/java/latest/jre/bin/java

  Indique para manter a seleção atual[+] ou digite o número da seleção:
</code></pre>

Neste caso, escolha a opção 2 (```/usr/java/jdk1.8.0_101/jre/bin/java```).

Para conferir se o JDK está instalado, digite o comando abaixo no terminal e verifique se a saída é parecida com esta:

<pre><code class="shell terminal">
$ java -version
  java version "1.8.0_101"
  Java(TM) SE Runtime Environment (build 1.8.0_101-b13)
  Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode)
</code></pre>

Agora vamos fazer um *Hello Word* para testar se está tudo funcionando. Abra um editor de texto e entre com o código fonte abaixo:

<pre><code class="java">
public class Main {
    public static void main(String[] args) {
    	System.out.println("Hello, World!");
    }
}
</code></pre>

Salve o arquivo com o nome ```Main.java``` e entre no diretório onde este se encontra para compilá-lo:

<pre><code class="shell terminal">
$ javac Main.java
</code></pre>

O compilador do **Java**, o **javac**, gerará um arquivo chamado ```Main.class```, para rodá-lo basta entrar com:

<pre><code class="shell terminal">
$ java Main
  Hello, World!
</code></pre>

Após a instalação do Java, talvez você também queira instalar o [Eclipse](/blog/como-instalar-eclipse-linux/) ;)
