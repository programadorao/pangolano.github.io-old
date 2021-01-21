---
layout: post
title: "Introdução ao PHP"
date: 2021-01-21 13:30:20 +0300
description: "Introdução a Linguagem PHP"
tags: [php, scripts, programação]
author: edgar
---

PHP é uma linguagem de alto nível, orientada à objectos server-side ou seja trabalha no lado do servidor.
PHP é usada para desenvolvimento de websites, normalmente ela é sempre acompanhada de outras duas linguagens "HTML e SQL".

Mas por enquanto vamos apenas focar no PHP, em outro momento falo sobre os seus companheiros.

Criada em 1994 por Rasmus Lerdof, hoje ela se encontra na sua 8ª versão, é uma das linguagens de programação mais populares em todo mundo e está em quase todo o lugar já que 79% dos sites usam ela. Então, quase oito a cada 10 websites que você visita na Internet estão usando PHP.
> Fonte [w3techs](https://w3techs.com/technologies/details/pl-php)

## INSTALANDO PHP

Se Gostou do breve resumo sobre PHP e quer instalar ela em sua máquina fique sabendo que é bem fácil de o fazer com apenas alguns cliques aqui e alí você estará pronto para escrever o seu primeiro "Olá Mundo" com PHP. 

A forma mais fácil de instalar o PHP na sua máquina é instalando o *XXAMPP*, este que é um pacote que possui os principais servidores de código aberto. Poderá baixar ele [clicando aqui](https://www.apachefriends.org/download.html), a sua instalação é bem simples SEGUINTE SEGUINTE E CONCLUÍDO!!. Você está quase no seu primeiro "Olá Mundo", depois de instalado você deverá iniciar o servidor do APACHE.

## Olá Mundo

Então Com o PHP instalado em sua máquina e o apache iniciado chegou a hora de dizer aquele "Olá Mundo" para quebrar a Maldição.
vamos até ao dir *C:\xampp\htdocs* e nele criar uma pasta chamada "projectophp".

Dentro desta Pasta iremos criar um ficheiro chamado index.php.

> index.php é o primeiro ficheiro que o servidor procura executar se não for pedido nenhum outro arquivo

Então já com todo o ambiente preparado chegou a hora de colocar a mão no código!!

{% highlight php %}
<?php
 echo "Olá Mundo";
?>
{% endhighlight %}

Com o apache iniciado e tudo feito abra o seu navegador e digite [http://localhost/projectophp](http://localhost/projectophp)

Então com esse trecho de código teremos nas nossas telas o nosso primeiro Olá Mundo, mas deixa explicar tudo isso.
Quando estamos a trabalhar com PHP todo o código
PHP deve estar entre `"<?php //seu codigo aqui ?>"`.

> <?php que é a tag/comando de abertura do código php e ?> o comando de fechamento/finalização do código

Então agora nos resta explicar o `"echo"` este que é um comando que serve para exibir/imprimir as coisas na tela, como foi mostrado no exemplo echo "Olá Mundo"; que exibiu na nossa tela um "Olá Mundo". 
Há não nos podemos esquecer do `";"` ele que indica onde a instrução ou comando termina! 
Sempre depois de uma instrução deverá finalizar com `";"` para indicar ao PHP que é o final da instrução e que pode executar a instrução seguinte.

## Váriaveis

Bom como em tudo na vida a gente tem que ter um lugar para podermos guardar as nossas coisas não é ? Temos a Carteira onde guardamos os nossos documentos, a sapateira onde guardamos os nossos sapatos e por aí fora. 
Com Programação não é diferente aqui nós temos às váriaveis!!

`"Váriavel"` é um espaço reservado na memória.

Podemos ver uma váriavel como uma gaveta onde você irá guardar a roupa!!

Vamos aprender a criar uma váriavel usando PHP

Para definir uma variável com PHP, basta digitar cifrão seguido do nome, sinal de igualdade e o valor($nome = "Edgar Singui").

{% highlight php %}
<?php
 $nome = "Edgar Singui";
?>
{% endhighlight %}

> O Sinal de igual serve como um atribuidor, podemos ler ele como recebe, então podemos ler essa instrução da seguinte forma "Váriavel nome recebe o valor Edgar Singui".

#### ATENÇÃO

Nomes de variáveis:

- Não podem começar com números
- Não podem começar com carácteres especiais 
- Não podem começar com palavras reservadas
- Não podem ter espaços.

## Exibindo Váriaveis

Agora que já sabemos criar uma váriavel e exibir um texto que tal exibir o texto armazenado em uma váriavel!!
É bem simples de se fazer a ideia é a seguinte,
1. Criar uma várivavel e atribuir a ela um valor.
2. Com o comando echo exibir o valor que está armazenado na váriavel.

{% highlight php %}
<?php
 $nome = "Edgar Singui";
 echo $nome; // Edgar Singui
?>
{% endhighlight %}

> Qualquer linha procedidade de // não é considerada pelo interpretador, então é um comentário.

Com apenas estes dois comandos teremos nas nossas telas o valor da váriavel sendo exibido.

## Resumo

Neste post você aprendeu:

1. História do PHP (Resumo)
2. Como instalar o PHP
3. Exibir valores
4. Criar Váriaveis

## Conclusão

O Post está ficando muito grande e eu não quero que você ache que programação é chato, então vou parar por aqui e nos vemos em outro post onde eu darei continuidade neste assunto!!
Se gostou do artigo não esqueça de partilhar. 
Se quiser que eu escreva sobre algo em específico deixe um comentário estaremos lendo.
