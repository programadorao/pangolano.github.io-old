---
title: Como fazer web scrapping com Python parte I
layout: post
date: '2021-01-14 00:50:12'
tags:
- python
- scripts
- beautifulsoup
- requests
- joa
author: joa
---

A web nos fornece dados que nenhum de nós conseguia ler ou entender. Muitas das vezes esses dados são fornecidos pelos criadores dos sites através de arquivos **.csv** ou de **API** (Aplication Program Interface).

Vou mostrar neste tutorial como raspar dados da web em python. Vamos utilizar dois pacotes muito conhecido na comunidade Python, [Requests](https://requests.readthedocs.io/en/master/) e [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/). O módulo Requests lhe permite integrar seus programas Python com serviços web, já o BeautiulSoup também conhecido como bs4 serve para coletar e *parsear*  arquivos html e xml(s).

## Requisitos
Neste tutorial não vou usar um ambiente virtual
[Como instalar ambiente virtual python3 ](https://www.treinaweb.com.br/blog/criando-ambientes-virtuais-para-projetos-python-com-o-virtualenv/)
Para concluir este tutorial com êxito você deve estar familiarizado com:
* Python3
* HTML
* Status code
* Importação de módulos python

Se tudo estiver ok vamos prosseguir...

## Instalar o Requests
Para trabalhar com requisições nós precisaremos do requests que é um módulo do Python trata disso de forma legível. 

> Em sistemas Linux é normal Python3 vir instalados e com alguns pacotes essencias já. Verifica se já tem o requests instalado antes de prosseguir

Vamos instala-lo com o pip:

```
pip install requests
```
Quando a instalação estiver em andamento verá a seguinte saida:

```
Collecting requests
  Downloading requests-2.18.1-py2.py3-none-any.whl (88kB)
    100% |████████████████████████████████| 92kB 3.1MB/s 
...
Installing collected packages: chardet, urllib3, certifi, idna, requests
Successfully installed certifi-2017.4.17 chardet-3.0.4 idna-2.5 requests-2.18.1 urllib3-1.21.1
```
Com requests instalado já podemos fazer nosso primeiro scrapping

Abre o Python no terminal e execute-o com o comando `python3` e importar o requests:
```
>>> import requests
```

Vamos atribuir a URL do Blog a variável url:
```
>>> url = "https://pangolano.github.io"
>>> pagina = request.get(url)
```
> `requests.get()` retorna um objecto e esse objecto foi atribuido a variável `pagina`

```
>>> pagina
<Response [200]>
>>>
```
O objecto Response retorna o código de estado 200 OK. Esse parâmetro pode ser acessado explicitamente com `pagina.status_code`
O código de retorno 200 nos diz que a página foi baixada com sucesso. Códigos que começam com o número 2 geralmente indicam sucesso, enquanto códigos que começam com 4 ou 5 indicam um erro ocorreu. Você pode ler mais sobre códigos de status[ HTTP nas Definições de Códigos de Status do W3C](https://www.w3.org/Protocols/HTTP/1.1/draft-ietf-http-v11-spec-01#Status-Codes).

Para trabalhar com dados da web, vamos querer acessar o conteúdo baseado em texto dos arquivos web. Podemos acessar os dados da resposta feita da seguinte forma:
```
>>> pagina.text
```
> <img src="{{site.baseurl}}/assets/img/gif/ue.jpg" alt="ué mas??" style="width: 300px; height:400px; margin: 0 auto;">
> 
> ué KKKKKKKKKKKKKK?

Antes de me ofender leia o próximo parágrafo :grinning:

O html do site apareceu de uma forma estranha e todo desorganizado, eu sei...
É aqui onde entra o papel do BeautifulSoup!!!
## Instalar BeautifulSoup
Instalar este pacote é tão simples quanto o **Requests**. Abre um outro terminal e digite:
```
pip install BeautifulSoup
```
Feito!!! Com o BS4 instalado na nossa máquina vamos importa-lo. Imaginemos que nosso terminal está assim:
```
>>> import requests
>>> url = "https://pangolano.github.io"
>>> pagina = request.get(url)
>>> pagina
<Response [200]>
>>> pagina.text
```
Vamos importar o  BeautifulSoup na variável `bs`
```
from bs4 import BeautifulSoup as bs
```
Esta é uma das diferentes formas e importação existente na linguagem Python. Eu citei acima que você deve estar familiarizado com importação de módulos para seguir o tutorial com êxito.

## Conclusão
Para evitar que o tutorial seja demasiado longo decidi fazer em partes. Enfim chegamos a fim de mais uma publicação, mas não do tópico. Em casos de dúvidas ou problemas na instalação de pacote acima citados comenta aqui ou no nosso grupo do Facebook.

## Extra
#### opcional :sleeping:
Caso já tenha conhecimento sobre o assunto este +++EXTRA+++ não fará muita diferença.

Vou fazer um resumo básico de como podemos importar módulos

Abaixo se segue várias formas de como importar módulos em Python:

Imaginamos que temos um módulo chamado pacote.py com seguinte código:
{% highlight python %}
class Mensagem():
	def __init__(self,msg):
		self.msg = msg
	def imprime(self):
		print(self.msg)

def mensagem():
	print("Oi")

{% endhighlight %}

{% highlight python %}
import pacote

pacote.Mensagem("Olá Mundo").imprimir()

mensagem()
{% endhighlight %} - importamos o arquivo todo e chamamos a classe `Mensagem`, passamos o argumento e imprimimos com o método `imprime()` e também executamos a função `mensagem()`.

{% highlight python %}
from pacote import *

pacote.Mensagem("Olá Mundo").imprimir()

mensagem()
{% endhighlight %} - importamos o arquivo todo e chamamos a classe `Mensagem`, passamos o argumento e imprimimos com o método `imprime()` e também executamos a função `mensagem()`.

{% highlight python %}
from pacote import Mensagem

Mensagem("Olá Mundo").imprimir()

{% endhighlight %} - importamos  a classe `Mensagem`, passamos o argumento e imprimimos com o método `imprime()`.

{% highlight python %}
from pacote import Mensagem as msg

msg("Olá Mundo").imprimir()

mensagem()
{% endhighlight %} - importamos a classe `Mensagem` em uma variável chamada `msg`, passamos o argumento e imprimimos com o método `imprime()` .

> Atenção!!! a importação em variáveis não funciona só com classe. Podemos usar em funções, listas, dicionários, etc.
> É só uma forma reduzida de querer se referir a função importada, ex.: `from bs4 import BeautifulSoup as bs`

{% highlight python %}
from pacote import mensagem

mensagem()
{% endhighlight %} -importamos a função com nome `mensagem` e executamos a função importada.

Acimas foram citadas algumas formas de importação de módulos/pacotes em Python. Leia a [documentação](https://docs.python.org/pt-br/3/tutorial/modules.html)

Nos vemos!!!
