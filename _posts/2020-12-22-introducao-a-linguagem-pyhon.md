---
layout: post
title: "Introdução à Python"
date: 2020-12-11 01:02:13 +
description: "Introdução sobre a linguagem de programação Python"
tags: [python, scripts, programação]
author: joa
---

Python é uma linguagem interpretada de alto nível, fortimente tipada e orientada à objectos.
Python é usada em diversas áreas como: Web, desktp, mobile, data science, inteligência artifial, machine learning, enfim, um infinito de coisas onde python é usado. 

Criada em 1991 pelo holandês Guido Van Rossun. Suporta banco de dados relacionais, é Free (GPL) e não depende de fornecedores exclusivos. Outro ponto, python é uma linguagem de script e interpretada

> Caso ainda não saiba, actualmente, Python tem duas verss mais utilizadas, Python 2 e Python 3. Python 3 é a versão mais actual. Dito isto, Python 3 é o futuro, então, não existe motivos para que você comece a programar com Python 2.

![Compilador - Interpretador]({{site.baseurl}}/assets/img/compilador-interpretador.png)

## INSTALANDO PYTHON
Instalar a linguagem python é muito fácil. Mostrarei dois métodos, um para windows e outro para linux.
Clica [aqui][instalacao-python] para ir aos slides de instalação

## OLÁ MUNDO
Agora que conhecemos um pouco da sua história e aspectos principais desta linguagem maravilhosa, vamos partir para o nosso primeiro código

{% highlight python %}
print("Olá mundo!")
{% endhighlight %}

Bora explicar esse trecho
`print()` - a função print serve para imprimir algo na tela. Esta mesma função recebe como parametro uma strin que nós usamos `"Olá mundo!"`

## VARIÁVEIS
Até aqui tudo calmo? rsrsrsr
Para definir uma variável no Python, basta digitar um nome, sinal de igualdade e o valor(nome = "Joaquim")
Vamos falar de variáveis, python é uma lingugem fortemente tipada nós não precisamos especificar seus tipos exemplo "int idade":

{% highlight python %}
idade = 17 #variável do tipo inteiro
altura = 1.87 #variável do tipo decimal ou real
nome = "Joa Roque" #variável do tipo string ou carácter
{% endhighlight %}

> Qualquer linha procedidade de # não é considerada pelo interpretador, então é um comentário.

#### ATENÇÃO

Nomes de variáveis:

- Não podem começar com números
- Não podem começar com carácteres especiais 
- Não podem começar com palavras reservadas


Alguns outros exemplos de variáveis e operações artimétricas

{% highlight python %}
>>> num1 = 1
>>> num2 = 5
>>> print(num1+num2) #saida será 6
>>> nome = "Joa"
>>> sobre_nome = "Roque"
>>> print(nome," ",sobre_nome)
{% endhighlight %}

**OPERADORES E SINAIS DE COMPARAÇÃO**

```
Operadores artimétricos
-----
+  : adição
-  : subtração
/  : divisão
*  : multiplicção
%  : resto da divisão
** : potenciação
-----
```
#### EXEMPLO:
{% highlight python %}
add = 5 + 5
sub = 5 - 4
div = 2020 / 2
multi = 2 * 2
pow = 2**2
print(add) # saida 10
print(sub) # saida 1
print(div) # saida 1010
print(multi) # saida 4
print(pow) # saida 4
{% endhighlight %}
Sinais de comparação
```
----
== : igual a
!= : diferente de
>  : maior que
<  : menor que
>= : maior ou igual a
<= : menor ou igual a
```
#### EXEMPLO
> Os sinais de comparação só retornam True e False(Verda)
{% highlight python %}
print(4 == 8) # saida False
print(4 != 2) # saida True
print(3 > 10) # saida False
print(20 < 10) # saida False
print(5 >= 8) # saida False
print(10 <= 30) # saida True
{% endhighlight %}

## ENTRADA DE DADOS


Aqui, aproveitamos para apresentar a função “input()”. Esta função é
utilizada para captar informações enviadas pelo usuário. Ela pode receber
um parâmetro, que será uma mensagem exibida ao usuário antes que ele
insira o que deseja.

A entrada inserida pelo usuário pode ser salva e utilizada posteriormente.
No exemplo abaixo, a entrada digitada pelo usuário é salva na variável
“nome” e depois é impressa, juntamente com a mensagem desejada. No
exemplo, logo após a exibição da mensagem “ Olá, qual o seu nome?”, o
programa aguardará o input do usuário. Após digitar seu nome, você deve
apertar o Enter, para que o código prossiga.

{% highlight python %}
nome = input("Olá, qual o seu nome?\n") 
print("Olá, %s" %nome)
> Olá, qual o seu nome?
Joaquim Roque
> Olá, Joaquim Roque
{% endhighlight %}

## CONCLUSÃO
Chegamos ao fim do post mas não do assunto. A publicação ficou muito extensa. Nos vemos!!!


[instalacao-python]: {{site.baseurl}}/tags/#programacao
