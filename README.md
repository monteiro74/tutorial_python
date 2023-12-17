# Tutorial sobre python


Objetivos: Pequenos exemplos para uso da linguagem python em sala de aula, em qualquer projetos de software. Exemplos que podem ser citados e comentados nas disciplinas que necessitam do apoio de uma linguagem de programação. Como prerequisito é necessário ter uma IDE instalada. Este material é extremamente resumido e supões que o leitor tem conhecimento básico de programação ou pelo menos português estruturado. (Esta é a versão: 2).<br>


```
Observações:
1. Este material pode ser usado como suporte às disciplinas de: lógica,
algoritmos, programação e projeto de sistemas.
2. Este material foi ou poderá ser usado em sala de aula/laboratório/EAD.
3. É um prerequisito conhecimentos básicos de programação e uso de 
IDE (os códigos foram testados com Spyder).
4. Os exemplos estão em python 3.
5. Esta página poderá passar por atualizações sem aviso prévio.
6. Se houver necessidade do uso de outras ferramentas de desenvolvimento 
de software além de python, consulte a lista de ferramentas:
https://github.com/monteiro74/lista_de_ferramentas
```

# Sumário:

# A - Conceitos e exemplos gerais da linguagem:<br>
[1. Comando print](#1-comando-print) <br>
[2. Comentário](#2-comentário) <br>
[3. Operações matemáticas](#3-operações-matemáticas) <br>
[3.1. Python com números](#31-python-com-números)<br>
[3.2. Exponenciação](#32-exponenciação)<br>
[3.3. Módulo](#33-módulo)<br>
[4. Tipos de dados e variáveis](#4-tipos-de-dados-e-variáveis)<br>
[4.1. Operações com strings](#41-operações-com-strings)<br>
[4.1.1. Concatenando strings](#411-concatenando-strings) <br>
[4.1.2. Tamanho de uma string](#412-tamanho-de-uma-string) <br>
[4.1.3. Percorrer uma string](#413-percorrer-uma-string) <br>
[4.1.4. Selecionando partes da string](#414-selecionando-partes-da-string) <br>
[4.1.5. String maiúsculo, capitalize, minúsculo](#415-string-em-minúsculo-capitalize-e-maiúsculo) <br>
[4.1.6. Função strip e split](#416-função-strip-split)<br>
[4.1.7. Buscas e substituição por strings](#417-busca-e-substituição-por-substring)<br>
[4.1.8. Formas de impressao de strings](#418-formas-de-impressao-de-string)<br>
[4.2. Variáveis locais e globais](#42-local-e-global)<br>
[5. Operadores](#5-operadores) <br>
[5.1. Operadores matemáticos](#51-operadores-matemáticos)<br>
[5.2. Operadores relacionais](#52-operadores-relacionais)<br>
[5.3. Operadores lógicos](#53-operadores-lógicos)<br>
[6. Tratamento de exceções](#6-tratamento-de-exceções)<br> 
[7. Estruturas condicionais](#7-estruturas-condicionais-controle-de-fluxo) <br>
[7.1. Break](#71-break)<br>
[7.2. Continue](#72-continue)<br>
[7.3. Pass](#73-pass)<br>
[7.4. Match case](#74-match-e-case)<br>
[8. Estruturas de repetição](#8-estruturas-de-repetição)<br>
[8.1. Laço while](#81-laço-while) <br>
[8.1.1. While true](#811-laço-while-true)<br>
[8.2. Laço for](#82-laço-for)<br>
[8.3. Laço for e range](#83-laço-for-e-range)<br> 
[9. Funções](#9-funções)<br>
[9.1. Definição de função](#91-documentação-de-função)<br>
[10. Arquivos](#10-arquivos)<br>
[10.1. Funções read, readline  readlines](#101-funções-read-readline-e-readlines)<br>
[10.2. Criar arquivos](#102-criar-arquivos)<br>
[11. Listas](#11-listas)<br>
[11.1. Acrescentando itens](#111-acessando-elementos-individuais-da-lista)<br> 
[11.2. Percorrer itens](#112-percorrer-elementos-de-uma-listas)<br> 
[11.3. Tamanho de listas](#113-tamanho-de-listas)<br> 
[11.4. Adicionar itens](#114-adicionando-itens-na-lista)<br> 
[11.5. Procurar um ítem](#115-procurar-um-elemento-na-lista)<br> 
[11.6. Substrair ítem](#116-subtraindo-elementos-de-uma-lista)<br> 
[11.7. Ordenando itens](#117-ordenando-itens-da-lista-sort)<br> 
[11.7.1. Sort crescente/decrescente](#1171-sort-decrescentedecrescente)<br>
[11.7.2. Sort invert](#1172-sort-inverter-itens)<br>
[11.8. Ordenando itens da lista](#118-ordenando-itens-da-lista-sorted)<br>
[11.9. Pop](#119-pop)<br>
[11.10. Funções para tratamento de listas](#1110-funções-para-tratamento-de-listas)<br>
[12. Tuplas](#12-tuplas)<br>
[13. Sets](#13-sets)<br>
[14. Dicionários](#14-dicionários)<br>
[14.1. Função items](#141-função-items)<br>
[14.2. Função values e keys](#142-função-values-e-keys)<br> 
[15. Comparação list, tuple, set e dictionary](#15-comparação-list-tuple-set-dictionary)<br>
[16. Números aleatórios](#16-números-aleatórios)<br>
[17. Arrays](#17-arrays)<br>
[18. Módulos](#18-módulos)<br>
[19. Inputs](#19-input)<br>
[20. Standard library](#20-standard-library)<br>

# B - Programação Orientada a Objetos<br>
[21. Python orientado a objetos](#21-python-orientado-a-objetos)<br>
[21.1. Instanciando objetos e atribuindo valores](#211-instanciando-objetos-atribundo-valores)<br>
[21.2. Sub classes e herança](#212-sub-classes-e-herança)<br>
[21.3. Encapsulação](#213-encapsulação)<br>
[21.4. Polimorfismo](#214-polimorfismo)<br>

# C - Banco MySQL(MariaDB)<br>
[22 Python com MySQL](#22-python-com-mysql)<br>
[22.1. SQL create database](#221-sql-create-database)<br>
[22.2. SQL create table](#222-sql-create-table)<br>
[22.3. SQL insert delete update](#223-sql-insert-delete-update)<br>
[22.4. Select](#224-sql-select)<br>
[22.5. Sum, Max, Min, Avg, Count](#225-sum-max-min-avg-count)<br>
[22.6. SQL drop table e drop databasae](#226-sql-drop-table-e-drop-database)<br>

# D - Banco MongoDB<br>
[23 Python com MongoDB](#23-python-com-mongodb)<br>

# E - Plot<br>
[24 Plot e gráfico](#24-plot-e-gráficos)<br>
[24.1. Gráfico com matplotlib](#241-gráfico-com-matplotlib)<br>
[24.2. Gráfico pizza](#242-gráfico-pizza)<br>
[24.2.1. Gráfico de pizza com matplotlib](#2421-gráfico-de-pizza-com-matplotlib)<br>
[24.3. Gráfico com numpy](#243-grafico-com-numpy)<br>
[24.4. Gráfico da distribuição normal](#244-gráfico-da-distribuição-normal)<br>
[24.5. Gráfico de dispersão](#245-gráfico-de-dispersão)<br>
[24.6. Gráfico boxplot com seaborn](#246-gráfico-boxplot-com-seaborn)<br>
[24.7 Gráfico de histograma](#247-gráfico-de-histograma)<br>
[24.8 Gráfico de histogramas com Seabor e KDE](#248-gráfico-de-histogramas-com-seabor-e-kde)<br>
[24.9. Gráfico com Matplotlib, KDE, Seaborn, pyplot](#249-gráfico-com-matplotlib-kde-seaborn-pyplot)<br>
[24.9.1. Gráfico de categorias com Seaborn e parâmetro kind](#2491-gráfico-de-categorias-com-seaborn-e-parâmetro-kind)<br>



# F - Estatísticas<br>
[25. Exemplos diversos com estatísticas](#25-exemplos-diversos-com-estatísticas)<br>
[25.1 Media, mediana, moda e desvio padrão](#251-media-mediana-moda-e-desvio-padrão)<br>
[25.2 Percentil e porcentagem](#252-percentil-e-porcentagem)<br>
[25.3. Regressão](#253-regressão)<br>
[25.3.1. Regressão linear](#2531-regressão-linear)<br>
[25.3.2. Regressão polinomial](#2532-regressão-polinomial)<br>
[25.4 Contagem de valores, média e mediana com pandas dataframe](#254-contagem-de-valores-média-e-mediana-com-pandas-dataframe)<br>
[25.5. Média, desvio padrão, mínimo, máximo. pandas dataframe](#255-média-desvio-padrão-mínimo-máximo-pandas-dataframe)<br>


# G - GUI<br>
[26 GUI com pyforms](#26-gui-com-pyforms)<br>



# H - Analise de dados
[27.1 Numpy](#271-numpy)<br>
[27.1.1 Geração de números randômicos](#2711-geração-de-números-randômicos)<br>
[27.1.2 Copy e View](#2712-copy-e-view)<br>
[27.1.3 Join, Split e Sort](#2713-join-split-e-sort)<br>
[27.2 Pandas](#272-pandas)<br>


<!--

[27.3. Seaborn](#273-seaborn)<br>
[27.4. Matplotlib](#274-matplotlib)<br>
[27.5. Scikitlearn]()<br>
[27.6. TensorFlow]()<br>
[27.7. Keras]()<br>
[27.8. Pytorch]()<br>
[27.9. Theano]()<br>
[27.10. MxNet]()<br>
[27.11. Café]()<br>
[27.12. CNT]()<br>
[27.13. Pillow]()<br>
[27.14. OpenCV]()<br>
[27.15. ApacheSpark]()<br>
[27.16 Hadoop]()<br>

[Voltar ao sumário](#sumário)<br>


## Desenvolvimento web
[28.1 Django]()<br>
[28.2. Flask]()<br>
[28.3. CherryPy]()<br>
[28.4. Pyramid]()<br>
[28.5. TurboGears]()<br>
[28.6. Falcon]()<br>
[28.7. Tornado]()<br>

[Voltar ao sumário](#sumário)<br>


## Desenvolvimento de app
[29.1. Kivy]()<br>
[29.2. BeeWare]()<br>
[29.3. Python-for-android]()<br>

[Voltar ao sumário](#sumário)<br>



## Web scraping
[30.1. urllib]()<br>
[30.2 requests]()<br>

[Voltar ao sumário](#sumário)<br>

## Interações com o site
[31.1. Selenium]()<br>
[31.2. Webbot]()<br>
[31.3. Webcrawler]()<br> 
[31.4. Scrapy]()<br>

[Voltar ao sumário](#sumário)<br>

-->

# Outros materiais:<br>
[Lista de IDEs](#lista-de-ides)<br>
[Lista de editores de códigos](#lista-de-editores-de-códigos)<br>
[Referências](#referências)<br>
[Comentários finais](#comentários-finais)<br>





---
# A - Conceitos e exemplos gerais da linguagem

# 1. Comando print

Impressão na tela, exemplo
```python
print("teste")
print("teste")
```

[Voltar ao sumário](#sumário)<br>



# 2. Comentário

Usando "#"

```python
# isto não é impresso
print("teste1")
""" isto não é impresso
print("teste2")
"""
print("teste3")
```

## 2.1. Codigo com acentos

```python
# -*- coding: utf8-8 -*-
print("Olá mundo!")
```

[Voltar ao sumário](#sumário)<br>



# 3. Operações matemáticas

```python
print(2+2)
print(2-2)
print(2*2)
print(2/2)
```

## 3.1. Python com números

O python utiliza 3 tipos numéricos: int, float e complex

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
inteiro1 = 35656222554887711
inteiro2 = -3255522
float1 = 7.35
float2 = -43.75
complexo1 = 1J 
complexo2 = 4.35 + 4.55j 

# em seguida realizamos as operações
print("Exemplo de inteiro: " + str(inteiro1))
print("Exemplo de inteiro: " + str(inteiro2))
print("Exemplo de float ou flutuante: " + str(float1))
print("Exemplo de float ou flutuante: " + str(float2))
print("Exemplo de complexo ou científico: " + str(complexo1))
print("Exemplo de complexo ou científico: " + str(complexo2))

```

O resultado será:

```python
Exemplo de inteiro: 35656222554887711
Exemplo de inteiro: -3255522
Exemplo de float ou flutuante: 7.35
Exemplo de float ou flutuante: -43.75
Exemplo de complexo ou científico: 1j
Exemplo de complexo ou científico: (4.35+4.55j)
```



## 3.2. Exponenciação

```python
print(2**3)
```

## 3.3. Módulo

```python
print(10/3)
```
O resultado é o resto
o operador é obtido pelo %

exemplo:

```python
print(10%3)
```


[Voltar ao sumário](#sumário)<br>



# 4. Tipos de dados e variáveis

Exemplo de uma variável com caracteres (strings)

```python
mensagem = "teste"
print(mensagem)
print(mensagem)
```
Regras para variáveis:
1. não pode ter espaço
2. não pode ter caracteres especiais
3. as variáveis são case sensitive
4. o sinal de = é chamado de operador de atribuição, não é um sinal ade igual !

Alguns exemplos de tipos de dados, mais comuns:

| Tipo de dado      | Exemplo |
| -----------       | ----------- |
| Número (Inteiro)      | 3       |
| Número flutuante (com decimais)  | 2.34        |
| String (texto) | "teste teste" |
| Boolean | TRUE ou FALSE |


Outros tipos:

* Numéricos:	int, float, complex <br>
* Sequenciais:	list, tuple, range <br>
* Mapeamento/mapa/map:	dict <br>
* Set (conjunto):	set, frozenset <br>
* Binary:	bytes, bytearray, memoryview <br>
* None:	NoneType <br>


Exemplo:

```python
var1 = 1 # isto é um comentario
var2 = 3.5 # estar variável é do tipo flutuante (inteiro com valor decimal)
var3 = "isto é uma string"
var4 = True
```

Se o código acima for executado, o resultado na tela será nada, pois apenas se armazenou os valores nas variáveis, não foram feitas nenhuma operação com elas.

Outro exemplo:

```python
var1 = 1 
var2 = 3.5 
var3 = "isto é uma string"
print(var1)
```

Se uma variável for declarada com um valor e posteriormente for feita outra declaração, a segunda declaração irá substituir a anterior.

No exemplo abaixo o valor 2 irá substituir o valor 1:

```python
var1 = 1 
var1 = 2 
print(var1)
```

[Voltar ao sumário](#sumário)<br>


## 4.1. Operações com strings

### 4.1.1. Concatenando strings

```python
# primeiro declaramos as variaveis
var1 = "aula"
var2 = "de"
var3 = "python"

# em seguida realizamos as operações
texto = var1 + " " + var2 + " " + var3
print(texto)
```

O resultado será:

```python
aula de python
```

[Voltar ao sumário](#sumário)<br>


### 4.1.2. Tamanho de uma string

```python
# primeiro declaramos as variaveis
var1 = "abc"
contar_letras = len(var1)

# em seguida realizamos as operações
print(contar_letras)

```

O resultado será:

```python
3
```

[Voltar ao sumário](#sumário)<br>


### 4.1.3. Percorrer uma string

```python
# primeiro declaramos as variaveis
var1 = "abcde"

# em seguida realizamos as operações
print(var1[3])
```

O resultado será:

```python
d
```

[Voltar ao sumário](#sumário)<br>



### 4.1.4. Selecionando partes da string

```python
# primeiro declaramos as variaveis
var1 = "abcdefghijklmno"

# em seguida realizamos as operações
print(var1[1:5])
```

O resultado será:

```python
bcde
```

[Voltar ao sumário](#sumário)<br>




### 4.1.5. String em minúsculo, capitalize e maiúsculo

```python
# primeiro declaramos as variaveis
var1 = "ABCDEFghijklm"

# em seguida realizamos as operações
print(var1.lower())
print(var1.capitalize())
print(var1.upper())
```

O resultado será:

```python
abcdefghijklm
Abcdefghijklm
ABCDEFGHIJKLM

```

[Voltar ao sumário](#sumário)<br>



### 4.1.6. Função strip, split

Strip, remove espaços em branco <br>



```python
# primeiro declaramos as variaveis
var1 = "   ABCDEFghijklm " 

# em seguida realizamos as operações
print(var1.strip())
```

O resultado será:

```python
ABCDEFghijklm
```

Split, converte a string em uma lista <br>

```python
# primeiro declaramos as variaveis
var1 = "uva, banana, arroz, carne, leite" 

# em seguida realizamos as operações
print(var1.split())
```

O resultado será:

```python
['uva,', 'banana,', 'arroz,', 'carne,', 'leite']
```

[Voltar ao sumário](#sumário)<br>


### 4.1.7. Busca e substituição por substring

Exemplo de buscas em strings

```python
# primeiro declaramos as variaveis
var1 = "uva, banana, arroz, carne, leite" 
substring1 = var1.find("carne")
substring2 = var1.find("feijao")

# em seguida realizamos as operações
print(substring1)
print(var1[substring1:])
print(substring2)
```

O resultado será:

```python
20
carne, leite
-1
```

Exemplo de substituição em strings

```python
# primeiro declaramos as variaveis
var1 = "uva, banana, arroz, carne, leite" 
var2 = "feijao"

# em seguida realizamos as operações
print(var1)
print(var1.replace("uva", var2))
```

O resultado será:

```python
uva, banana, arroz, carne, leite
feijao, banana, arroz, carne, leite
```

[Voltar ao sumário](#sumário)<br>


### 4.1.8. Formas de impressao de string

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
var1 = "Tutorial"
var2 = "sobre"
var3 = "python"

# em seguida realizamos as operações
print("Tutorial sobre python")
print(var1, var2, var3)
print("Este é um {} {} {}".format(var1, var2, var3))
print(f"Este é um {var1} {var2} {var3}")
```

O resultado será:

```python
Tutorial sobre python
Tutorial sobre python
Este é um Tutorial sobre python
Este é um Tutorial sobre python
```

[Voltar ao sumário](#sumário)<br>



## 4.2. Local e Global

Variáveis locais e globais ou escopo local e global.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
x = "global"

def funcao1():
  x = "local"
  print("Exemplo de variavel: " + x)

# em seguida realizamos as operações
funcao1()
print("Exemplo de variavel: " + x)
```

O resultado será:

```python
Exemplo de variavel: local
Exemplo de variavel: global
```

[Voltar ao sumário](#sumário)<br>




# 5. Operadores

Recordando que = é um operador de atribuição.

## 5.1. Operadores matemáticos

Revisão de alguns operadores..

| Operador     | Operação |
| ----------- | ----------- |
| +      | Soma      |
| -  | Subtração        |
| * | Multiplicação |
| / | Divisão |
| ** | Exponenciação |
| % | Módulo |

## 5.2. Operadores relacionais

Operadores relacionais são usados para fazer comparações, por exemplo:

| Operador     | Operação |
| ----------- | ----------- |
| == | Igualdade      |
| !=  | Diferença        |
| > | Maior que |
| < | Menor que |
| >= | Maior ou igual |
| <= | Menor ou igual |

exemplos:

```python
# primeiro declaramos as variaveis
var1 = 5 
var2 = 2 

# em seguida realizamos as operações
print(var1 == var2)
print(var1 != var2)
print(var1 > var2)
print(var1 < var2)
print(var1 >= var2)
print(var1 <= var2)
```

O resultado acima será:
```python
False
True
True
False
True
False
```

[Voltar ao sumário](#sumário)<br>


## 5.3. Operadores lógicos

Permite comparações entre valores das variáveis

| Operador     | Operação |
| ----------- | ----------- |
| OR | Ou, ao menos uma condição é verdadeira |
| AND  | E, ambas condições são verdadeiras |
| NOT | Negação, inverter valor |

Exemplos:

```python
# primeiro declaramos as variaveis
var1 = 5 
var2 = 2 
var3 = 1
var4 = 1

# em seguida realizamos as operações
print(var1 == var2 and var1 == var3)
print(var3 == var4)
```

O resultado acima será:
```python
False
True
```

[Voltar ao sumário](#sumário)<br>




# 6. Tratamento de exceções

```python
# declarações/atribuições
a = 2
b = 0
# em seguida realizamos as operações
try:
    print(a/b)
```

O resultado será:

```python
SyntaxError: expected 'except' or 'finally' block
```

```python
# declarações/atribuições
a = 2
b = 0
# em seguida realizamos as operações
try:
    print(a/b)
except:
    print("ocorreu um erro!")
```

O resultado será:

```python
ocorreu um erro!
```

[Voltar ao sumário](#sumário)<br>




# 7. Estruturas condicionais (controle de fluxo)

Também chamados de comandos estruturais.
Servem para realizar avaliações ou testes entre variáveis.

Depois de uma condiçõa existe um bloco de código criado com uma tabulação.

exemplos:

```python
# primeiro declaramos as variaveis
var1 = 5 
var2 = 2 
var3 = 1
var4 = 1

# em seguida realizamos as operações
if var1 > var4:
    print("a var1 é maior que var4")
    
if var1 < var4:
    print("a var1 é menor que var4")
```

O resultado acima será:

```python
a var1 é maior que var4
```

no exemplo acima somente um dos if é executado se a condição verdadeira ocorrer.

Outro exemplo com if...else...

```python
# primeiro declaramos as variaveis
var1 = 1 
var2 = 3 

# em seguida realizamos as operações
if var1 > var2:
    print("a var1 é maior que var2")
else:    
    print("a var1 é menor que var2")
```

O resultado acima será:
```python
a var1 é menor que var2
```

Outro exemplo com elif:

```python
# primeiro declaramos as variaveis
var1 = 1 
var2 = 3

# em seguida realizamos as operações
if var1 == var2:
    print("numeros iguais")
elif var1 < var2:
    print("var1 menor que var2")
elif var2 > var1:
    print("var2 maior que var1")
else:
    print("valores não sao iguais")
```

O resultado acima será:
```python
var1 menor que var2
```


Outro exemplo com elif:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
x = int(input("Digite um numero: "))

# em seguida realizamos as operações
if x < 0:
    x = 0
    print('fornecido numero negativo')
elif x == 0:
    print('Zero')
elif x == 1:
    print('Um')
else:
    print('Maior que um')
```

O resultado acima será:
```python
Maior que um
```

[Voltar ao sumário](#sumário)<br>

## 7.1. Break


```python
# -*- coding: utf-8 -*-

for num in range(1, 11):
    print(num)
    if num == 5:
        break
```

O resultado acima será:
```python
1
2
3
4
5
```

[Voltar ao sumário](#sumário)<br>

## 7.2. Continue

```python
# -*- coding: utf-8 -*-
for numero in range(1, 10):
    print(numero)
    if numero % 2 == 0:
        print("numero par", numero)
        continue    
    if numero == 5:
        break
```

O resultado acima será:
```python
1
2
numero par 2
3
4
numero par 4
5
```

[Voltar ao sumário](#sumário)<br>




## 7.3. Pass

Pass pode ser usado quando existe a necessita de uma comando/parâmetro, mas ele não tratá efeito e requerer uma ação.

```python
# -*- coding: utf-8 -*-
numero = 0
while True:
    pass
    for numero in range(1,21):
        print(numero)
        if numero == 4:
            break
    break
```

O resultado acima será:
```python
1
2
3
4
```

Também pode ser usando para permitir uma classe tenha um conteúdo inicial enquanto o restanto do projeto da classe não esta totalmente pronto.

```python
# -*- coding: utf-8 -*-
class Classe1:
    pass
```

[Voltar ao sumário](#sumário)<br>




## 7.4. Match e case

Match e case, são equivalentes ao Swtich do C# e Java.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
escolha = input("Digite um número de 1 a 4 ")

# operações
match escolha:
    case "1":
        print("Digitado: 1")

    case "2":
        print("Digitado: 2")

    case "3":
        print("Digitado: 3")

    case "4":
        print("Digitado: 4")

    case _:
        print("Nenhum das alternativas")
```

O resultado acima será:
```python
Digite um número de 1 a 4 2
Digitado: 2
```

[Voltar ao sumário](#sumário)<br>


# 8. Estruturas de repetição

Também são chamados de laços de repetição ou iteradores. Iterar é repetir. Desta forma um bloco (ou várias linhas de código) serão repetidas até que uma condição seja satisfeita.<br>

## 8.1. Laço while

```python
# primeiro declaramos as variaveis
var1 = 1 

# em seguida realizamos as operações
while var1 < 10:
    print(var1)
    var1 = var1+2
     
print("------------")    
    
# primeiro declaramos as variaveis
var2 = 5

# em seguida realizamos as operações
# x= é o mesmo que x=x+1
while var2 < 8:
    print(var2)
    var2 += 1
```

O resultado acima será:
```python
1
3
5
7
9
------------
5
6
7
8
9
```

[Voltar ao sumário](#sumário)<br>




### 8.1.1. Laço while true

```python
# -*- coding: utf-8 -*-
numero = 0
while True:
    for numero in range(1,21):
        print(numero)
        if numero == 4:
            break
    break
```

O resultado acima será:
```
1
2
3
4
```

[Voltar ao sumário](#sumário)<br>


## 8.2. Laço for

Este laço usado para percorrer uma estrutura de dados, como uma lista, por exemplo:

```python
# declarações/atribuições
primeira_lista = [1,2,3,"ana","bob",True,5.66,0,abc]

# em seguida realizamos as operações
for i in primeira_lista:
    print(i)
```

O resultado acima será:
```python
1
2
3
4
ana
bob
True
5.66
0
3
```

[Voltar ao sumário](#sumário)<br>



## 8.3. Laço for e range

```python
# em seguida realizamos as operações
# conta de 5 até 15 pulando 3 valores
for i in range (5,15,3):
    print(i)
```

O resultado será:

```python
5
8
11
14
```

[Voltar ao sumário](#sumário)<br>



# 9. Funções

Funções são blocos de código. Em python uma função vem precedida da palavra def, seguido do nome e os parâmetros da função. Uma função que já foi utilizada com frequencia até o momento foi print(). O bloco de comandos vai depois de uma tabulação.

Exemplo:

```python
# primeiro declaramos a função
def soma(valor1, valor2):
    print(valor1)
    print(valor2)
    return valor1 + valor2

def subtracao(valor1, valor2):
    print(valor1)
    print(valor2)
    return valor1 - valor2
    
# em seguida realizamos as operações
resultado1 = soma(1, 5)
resultado2 = subtracao(7, 3)
print("----")
print(resultado2)

```

O resultado será:

```python
1
5
7
3
----
4
```

## 9.1. Função recursiva

Exemplo de chamada recursiva:

```python
# primeiro declaramos a função
def soma(valor1, valor2):
    print(valor1)
    print(valor2)
    return valor1 + valor2


def subtracao(valor1, valor2):
    print(valor1)
    print(valor2)
    return valor1 - valor2
    
    
# em seguida realizamos as operações
resultado1 = soma(1, 5)
resultado2 = subtracao(7, 3)
print("----")
print(resultado2)
print("exemplo de chamada recursiva:")
print(soma(resultado1, resultado2))

```

O resultado será:

```python
1
5
7
3
----
4
exemplo de chamada recursiva:
6
4
10
```

[Voltar ao sumário](#sumário)<br>


## 9.2. Documentação de função


```python
# -*- coding: utf-8 -*-
# declarações/atribuições
def funcao1():
    """
    Chamada a função funcao1
    """
    pass

# operações
print(funcao1.__doc__)
```

O resultado será:

```python
Chamada a função funcao1
```

[Voltar ao sumário](#sumário)<br>



# 10. Arquivos

O python pode manipular arquivos. Para abrir um arquivo é utilizada a função open. Os modos de trabalho com arquivos são: <br>


|Modo|	Descrição|
| --- | --- |
| r	| Abre o arquivo para leitura, é o default |
| w	| Abre o arquivo para leitura; criar um arquivo se o arquivo não existe ou troca o arquivo se existe.|
| x	| Abra um arquivo para criação exclusiva. Se o arquivo já existir, a operação falhará |
| a | Abra um arquivo para anexar no final do arquivo sem truncá-lo. Cria um novo arquivo se ele não existir. |
| t | Abre o arquivo em modo texto (default) |
| b | Abre um arquivo em modo binário. |



## 10.1. Funções read, readline e readlines

Exemplo de uso das funções para manipular arquivos:

```python
# declarações/atribuições
arquivo1 = open("arquivo_teste.txt")    
    
# operações
print(arquivo1)
```

O resultado será:

```python
<_io.TextIOWrapper name='arquivo_teste.txt' mode='r' encoding='cp1252'>
```

### 10.1.1. Função readlines

Exemplo do uso de readlines:

```python
# declarações/atribuições
arquivo1 = open("arquivo_teste.txt")    
linhas1 = arquivo1.readlines()
    
# operações
print(linhas1)
```

O resultado será:

```python
['caneta\n', 'apagador\n', 'caderno']
```

Outro exemplo com for para percorrer todo o arquivo:

```python
# declarações/atribuições
arquivo1 = open("arquivo_teste.txt")    
conteudo1 = arquivo1.readlines()
    
# operações
for linha1 in conteudo1:
    print(linha1)
```

O resultado será:

```python
caneta

apagador

caderno
```

[Voltar ao sumário](#sumário)<br>

### 10.1.2. Função read

```python
# declarações/atribuições
arquivo1 = open("arquivo_teste.txt")    
conteudo1 = arquivo1.read()
    
# operações
print(conteudo1)
```

O resultado será:

```python
caneta
apagador
caderno
```

Outros exemplos:

Retorna apenas uma linha do arquivo selecionado.<br>
Usa como parâmetro o número de bytes que deverá retornar, -1 significa tudo.

```python
# declarações/atribuições
arquivo1 = open("arquivo_teste.txt")    
conteudo1 = arquivo1.readline(-1)
    
# operações
print(conteudo1)
```

O resultado será:

```python
caneta
```

[Voltar ao sumário](#sumário)<br>



## 10.2. Criar arquivos

O parâmetro w esta criando o arquivo.

```python
arquivo2 = open("arquivo_teste2.txt", "w")    

arquivo2.write("primeira informação dentro do arquivo_teste2")

arquivo2.close()
```

O resultado poderá ser visto na pasta onde o programa foi chamado, lá deverá haver um arquivo .txt novo.

O parâmetro a adiciona uma nova linha no final do arquivo preexistente.

```python
arquivo2 = open("arquivo_teste2.txt", "a")    

arquivo2.write("primeira informação dentro do arquivo_teste2 !!!! \n")

arquivo2.close()
```

[Voltar ao sumário](#sumário)<br>





# 11. Listas

São um conjunto de dados para armazenar multiplos itens em uma única variável.


```python
# declarações/atribuições
lista1 = ["feijao", "arroz", "carne"]

# operações
print(lista1)
```

O resultado será:

```python
['feijao', 'arroz', 'carne']
```

[Voltar ao sumário](#sumário)<br>



## 11.1. Acessando elementos individuais da lista

Neste exemplo, queremos acessar um elemento específico da lista:

```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
print(lista1[4])
print(lista1[5])
```

O resultado será:

```python
ARROZ
Carne
```

Se for solicitado um elemento fora da lista, o interpretador irá apresentar um erro dizendo que o índice esta fora da faixa de valores.

```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
print(lista1[9])
```

O resultado será:

```python
IndexError: list index out of range
```

[Voltar ao sumário](#sumário)<br>



## 11.2. Percorrer elementos de uma listas

Usando o laço for:

```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
for item in lista1:
    print(item)
```

O resultado será:

```python
1
2
3
4
ARROZ
Carne
3.78
False
True
```

[Voltar ao sumário](#sumário)<br>



## 11.3. Tamanho de listas

Para descobrir o tamanho (em quantidade de elementos) de uma lista, utiliza-se a função len.


```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
print(len(lista1))
```

O resultado será:

```python
9
```

[Voltar ao sumário](#sumário)<br>

## 11.4. Adicionando itens na lista


```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
lista1.append("item_adicionado")
print(lista1)
```

O resultado será:

```python
[1, 2, 3, 4, 'ARROZ', 'Carne', 3.78, False, True, 'item_adicionado']
```

[Voltar ao sumário](#sumário)<br>


## 11.5. Procurar um elemento na lista

```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
if 3 in lista1:
    print("elemento 3 encontrado")

if "ARROZ" in lista1:
    print("elemento ARROZ encontrado")
```

O resultado será:

```python
elemento 3 encontrado
elemento ARROZ encontrado
```

[Voltar ao sumário](#sumário)<br>

## 11.6. Subtraindo elementos de uma lista

```python
# declarações/atribuições
lista1 = [1,2,3,4,"ARROZ", "Carne", 3.78, False, True]
        
# em seguida realizamos as operações
print("Lista completa: ")
print(lista1)
print("Removido o item 5: ")
del lista1[5] # remove o item 5
print(lista1)
print("Remove tudo a partir do item 5: ")
del lista1[5:] # remove a partir do item 5
print(lista1)
print("Apaga todos os itens da lista")
del lista1[:] # remove todos os itens
print(lista1)
```

O resultado será:

```python
Lista completa: 
[1, 2, 3, 4, 'ARROZ', 'Carne', 3.78, False, True]
Removido o item 5: 
[1, 2, 3, 4, 'ARROZ', 3.78, False, True]
Remove tudo a partir do item 5: 
[1, 2, 3, 4, 'ARROZ']
Apaga todos os itens da lista
[]
```

[Voltar ao sumário](#sumário)<br>



## 11.7. Ordenando itens da lista, sort

```python
# declarações/atribuições
lista1 = [7,8,4,3,5,6,9,2]
        
# em seguida realizamos as operações
lista1.sort()
print(lista1)
```

O resultado será:

```python
[2, 3, 4, 5, 6, 7, 8, 9]
```

[Voltar ao sumário](#sumário)<br>



### 11.7.1. Sort decrescente/decrescente

```python
# declarações/atribuições
lista1 = [7,8,4,3,5,6,9,2]

# em seguida realizamos as operações
print("Imprime decrescente: ")
lista1.sort(reverse=True)
print(lista1)
print("Imprime crescente: ")
lista1.sort(reverse=False)
print(lista1)
```

O resultado será:

```python
Imprime decrescente: 
[9, 8, 7, 6, 5, 4, 3, 2]
Imprime crescente: 
[2, 3, 4, 5, 6, 7, 8, 9]
```

[Voltar ao sumário](#sumário)<br>

### 11.7.2. Sort inverter itens


```python
# declarações/atribuições
lista1 = [7,8,4,3,5,6,9,2]

# em seguida realizamos as operações
lista1.reverse()
print(lista1)
```

O resultado será:

```python
[2, 9, 6, 5, 3, 4, 8, 7]
```

[Voltar ao sumário](#sumário)<br>

## 11.8. Ordenando itens da lista, sorted

```python
# declarações/atribuições
lista1 = [7,8,4,3,5,6,9,2]
nova_lista2 = sorted(lista1)        

# em seguida realizamos as operações
print(nova_lista2)
```

O resultado será:

```python
[2, 3, 4, 5, 6, 7, 8, 9]
```

[Voltar ao sumário](#sumário)<br>



## 11.9. Pop

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [7,8,4,3,5,6,9,2]

# em seguida realizamos as operações
print("Imprime lista: ")
lista1.sort()
lista1.pop()
print(lista1)
lista1.sort()
lista1.pop()
print(lista1)
lista1.sort()
lista1.pop()
print(lista1)
lista1.sort()
lista1.pop()
print(lista1)
```

O resultado será:

```python
[2, 3, 4, 5, 6, 7, 8]
[2, 3, 4, 5, 6, 7]
[2, 3, 4, 5, 6]
[2, 3, 4, 5]
```

[Voltar ao sumário](#sumário)<br>




---
## 11.10. Funções para tratamento de listas

Exemplo no uso de funções para tratamento de listas:

### 11.10.1. List comprehensions

É uma funcionalidade que permite a geração de novas listas.

Exemplo 1: sem list comprehension

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]
lista2 = []

# em seguida realizamos as operações
for i in lista1:
    lista2.append(i**2)

print(lista1)
print(lista2)
```

* Atenção: a letra "i" é usada para representar um indice, pode-se reescrever o código acima da seguinte forma:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]
lista2 = []

# em seguida realizamos as operações
for indice in lista1:
    lista2.append(indice**2)

print(lista1)
print(lista2)
```

O resultado de ambos os códigos (usando "i" ou "indice" ou "melancia") será o mesmo:

```python
[4, 5, 7, 8, 9, 0]
[16, 25, 49, 64, 81, 0]
```

Exemplo 2: com list comprehension

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]
lista2 = [i**2 for i in lista1]

# em seguida realizamos as operações
print(lista1)
print(lista2)
```

O resultado será:

```python
[4, 5, 7, 8, 9, 0]
[16, 25, 49, 64, 81, 0]
```

Exemplo 2: com list comprehension e com uma condição, neste exemplo gera uma nova lista com números pares.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]
lista2 = [i**2 for i in lista1]
lista3 = [i for i in lista1 if i%2==0]

# em seguida realizamos as operações
print(lista1)
print(lista2)
print(lista3)
```

O resultado será:

```python
[4, 5, 7, 8, 9, 0]
[16, 25, 49, 64, 81, 0]
[4, 8, 0]
```

[Voltar ao sumário](#sumário)<br>



### 11.10.2. Função Enumerate

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]

# em seguida realizamos as operações
for indice in lista1:
    print(indice)
```

O resultado será:

```python
4
5
7
8
9
0
```

Outro exemplo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]

# em seguida realizamos as operações
for indice in range(len(lista1)):
    print(indice, lista1[i])
```

O resultado será:

```python
0 4
1 5
2 7
3 8
4 9
5 0
```

Outro exemplo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [4,5,7,8,9,0]

# em seguida realizamos as operações
for indice, valor_numerico in enumerate(lista1):
    print(indice, valor_numerico)
```

O resultado será:

```python
0 4
1 5
2 7
3 8
4 9
5 0
```

[Voltar ao sumário](#sumário)<br>






### 11.10.3. Função Map

Esta função aplica uma função aos elementos de uma lista.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
def duplicar(x):
    return x*2

lista1 = [1,3,5,7,8,9]

lista2 = map(duplicar, lista1)
lista2 = list(lista2)

# em seguida realizamos as operações
print(lista2)
```

O resultado será:

```python
[2, 6, 10, 14, 16, 18]
```

[Voltar ao sumário](#sumário)<br>






### 11.10.4. Função Reduce

Permite aplica uma função especificada a todos os argumentos de uma lista.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
from functools import reduce

def soma_valores_da_lista(valor1, valor2):
    return valor1 + valor2

lista1 = [1,3,5,7,8,9]

soma1 = reduce(soma_valores_da_lista, lista1)

# em seguida realizamos as operações
print(soma1)
```

O resultado será:

```python
33
```

[Voltar ao sumário](#sumário)<br>




### 11.10.5. Função Zip

A função zip permite que itens possam "juntados" a partir de duas listas anteriores, criar uma nova lista com a junção destes.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
lista1 = [5,6,7,8,9,10]
lista2 = ["a","b","c","d","e"]
lista3 = ["casa", "carro", "cadeira", "mesa", "porta"]

# em seguida realizamos as operações
for valor1, valor2, valor3 in zip(lista1, lista2, lista3):
    print(valor1, valor2, valor3)

```

O resultado será:

```python
5 a casa
6 b carro
7 c cadeira
8 d mesa
9 e porta
```

[Voltar ao sumário](#sumário)<br>




# 12. Tuplas

Lista são dinâmicas e tuplas estáticas!

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
tupla1 = ("banana", "abacate", "melancia", "abacate")

# em seguida realizamos as operações
print(tupla1)
print("comprimento: ",len(tupla1))
```

O resultado será:

```python
('banana', 'abacate', 'melancia', 'abacate')
comprimento:  4
```

[Voltar ao sumário](#sumário)<br>


# 13. Sets

Com os conjuntos é possível armazenar multiplos valores em uma única variável. Os conjuntos não podem ser ordenados.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
set1 = ("banana", "abacate", "melancia")

# em seguida realizamos as operações
print(set1)
```

```python
('banana', 'abacate', 'melancia')
```

[Voltar ao sumário](#sumário)<br>


# 14. Dicionários

O dicionário é um conjunto de elementos do tipo chave e valor. O dicionário não obedece uma ordem.


```python
# declarações/atribuições
declaracoes1 = {"A":"ANA", "B":"BOB", "C":"CARLOS", "D":"DANIEL"}

# em seguida realizamos as operações
print(declaracoes1)
print(declaracoes1["B"])
print("--- imprime as chaves ---")
for chaveD in declaracoes1:
    print(chaveD)
print("--- impime os valores ---")
for chaveD in declaracoes1:
    print(declaracoes1[chaveD])
print("--- impime chave e valores ---")
for chaveD in declaracoes1:
    print(chaveD + ":" +  declaracoes1[chaveD])
```

O resultado será:

```python
{'A': 'ANA', 'B': 'BOB', 'C': 'CARLOS', 'D': 'DANIEL'}
BOB
--- imprime as chaves ---
A
B
C
D
--- impime os valores ---
ANA
BOB
CARLOS
DANIEL
--- impime chave e valores ---
A:ANA
B:BOB
C:CARLOS
D:DANIEL
```

[Voltar ao sumário](#sumário)<br>



## 14.1. Função items

```python
# declarações/atribuições
declaracoes1 = {"A":"ANA", "B":"BOB", "C":"CARLOS", "D":"DANIEL"}

# em seguida realizamos as operações
for chaveD in declaracoes1.items():
    print(chaveD)
```

O resultado será:

```python
('A', 'ANA')
('B', 'BOB')
('C', 'CARLOS')
('D', 'DANIEL')
```

[Voltar ao sumário](#sumário)<br>




## 14.2. Função values e keys

```python
# declarações/atribuições
declaracoes1 = {"A":"ANA", "B":"BOB", "C":"CARLOS", "D":"DANIEL"}

# em seguida realizamos as operações
for chaveD in declaracoes1.values():
    print(chaveD)
```

O resultado será:

```python
ANA
BOB
CARLOS
DANIEL
```

agora com a função keys

```python
# declarações/atribuições
declaracoes1 = {"A":"ANA", "B":"BOB", "C":"CARLOS", "D":"DANIEL"}

# em seguida realizamos as operações
for chaveD in declaracoes1.keys():
    print(chaveD)
```

O resultado será:

```python
A
B
C
D
```

[Voltar ao sumário](#sumário)<br>



# 15. Comparação List, Tuple, Set, Dictionary

| List | Tuple | Dictionary | Set
| --- | --- | --- | --- |
| Permite itens duplicados | Permite itens duplicados | Sem duplicados | Sem duplicados |
| Mutável | Não mutável | Mutável, indexável | Não pode ser mudada, mas pode ser adicionada, não indexada|
| Ordenada | Ordenada | Não ordenada | Não ordenada |
| [] ou list() | () ou tuple() | {}* ou set() | {} ou dict()|

Fonte: https://www.devopsschool.com/blog/python-tutorials-difference-between-list-array-tuple-set-dict/




# 16. Números aleatórios


```python
# -*- coding: utf-8 -*-
# importando módulos
import random

# declarações/atribuições
n1 = random.randint(0,50)

# em seguida realizamos as operações
print(n1)
```

O resultado será um inteiro:

```python
17
```

Outro exemplo:


```python
# -*- coding: utf-8 -*-
# importando módulos
import random

# declarações/atribuições
# random.seed(2)
n1 = random.randint(0,50)

lista1 = [3,5,7,8,9]
n2 = random.choice(lista1)

# em seguida realizamos as operações
print(n1)
print(n2)
```

O resultado poderá ser:

```python
13
9
```

[Voltar ao sumário](#sumário)<br>




# 17. Arrays

Python não tem suporte a arrays (matrizes), veja listas.

[Voltar ao sumário](#sumário)<br>




# 18. Módulos

Os módulos são outros programas feitos em python que podem ser chamados, é uma forma de se estruturar funções em bibliotecas de códigos separados em outros arquivos.

O primeiro arquivo será o modulo1.py

```python
# -*- coding: utf-8 -*-
# modulo1

def imprimindo(variavel1):
    print("a variavel recebeu o valor: ", variavel1)
```

O arquivo principal, será colocado na mesma pasta que o arquivo anterior. O arquivo principal esta a seguir:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import modulo1

# em seguida realizamos as operações
modulo1.imprimindo("abcde")
```

O resultado será:

```python
a variavel recebeu o valor:  abcde
```

[Voltar ao sumário](#sumário)<br>








# 19. Input


```python
# -*- coding: utf-8 -*-
# declarações/atribuições
palavra1 = input("Digite uma palavra: ")

# em seguida realizamos as operações
print("Foi digitado: " + palavra1)
```

O resultado será:

```python
Digite uma palavra: teste
Foi digitado: teste
```

[Voltar ao sumário](#sumário)<br>



# 20. Standard Library

A documentação oficial esta em: https://docs.python.org/3/library/

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import math
valor = 5

# em seguida realizamos as operações
print("conseno: ", math.cos(valor))
print("seno: ", math.sin(valor))
print("tangente: ", math.tan(valor))
```

O resultado será:

```python
conseno:  0.28366218546322625
seno:  -0.9589242746631385
tangente:  -3.380515006246586
```

```
Atenção: adicionar mais exemplos da standard library.
```

[Voltar ao sumário](#sumário)<br>


---
# B - Programação Orientada a Objetos

# 21. Criando classes

Criando uma classe sem atributos e sem métodos:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:

    def __init__(self):
        pass
```

Criando os atributos de uma classe:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:

    def __init__(self, nome, idade):  
        self.nome = nome
        self.idade = idade

```

Criando os métodos de uma classe:


```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:

    def __init__(self, nome, idade):  
        self.nome = nome
        self.idade = idade
    
    def caminhar(self):
        print("caminhando...")

    def andar(self): # métodos
        print("andar...")
```



Outro exemplo simplificado abaixo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:
    # atributos da classe
    nacionalidade = "brasileiro"

    # metodos construtor
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    # metodo descricao
    def descricao(self):
        return f"{self.nome} tem {self.idade} anos de idade"

    # metodo fala
    def fala(self, fale):
        return f"{self.nome} diz {fale}"

# outro exemplo de classe
class Pet:
  pass

# +1 exemplo de classe
class Carro:
  pass

# duas instanciações como exemplo
ana = Pessoa("ana", 33)
beth = Pessoa("beth", 25)

# em seguida realizamos as operações
print("nome: ", ana.nome)
print("nacionalidade: ", ana.nacionalidade)
print("idade: ", ana.idade)
print("--------------------------")
print("nome: ", beth.nome)
print("nacionalidade: ", beth.nacionalidade)
print("idade: ", beth.idade)
```

O resultado será:

```python
nome:  ana
nacionalidade:  brasileiro
idade:  33
--------------------------
nome:  beth
nacionalidade:  brasileiro
idade:  25
```

[Voltar ao sumário](#sumário)<br>



## 21.1. Instanciando objetos, atribuindo valores

Exemplo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:

    # classe atributo
    nome = ""
    idade = 0

# cria o objeto ana
ana = Pessoa()
ana.nome = "ana"
ana.idade = 20

# cria o objeto pedro
pedro = Pessoa()
pedro.nome = "pedro"
pedro.idade = 30

# em seguida realizamos as operações:
    
# imprimindo os valores do objetos
print(f"{ana.nome} tem {ana.idade} anos")
print(f"{pedro.nome} tem {pedro.idade} anos")
```

O resultado será:

```python
ana tem 20 anos
pedro tem 30 anos
```

[Voltar ao sumário](#sumário)<br>



## 21.2. Sub classes e herança

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:
    # atributos da classe
    nacionalidade = "brasileiro"

    # metodos construtor
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    # metodo descricao
    def descricao(self):
        return f"{self.nome} tem: {self.idade} anos de idade"

    # metodo fala
    def fala(self, fale):
        return f"{self.nome} diz: {fale}"

# classe derivada
class Cyborg(Pessoa):
    fabricante = "tecnologia nacional"
    tipo = "robo humanoide"
    def correr(self):
        return("Humanoide pode correr")

ana = Pessoa("ana", 33)
b9 = Cyborg("robo b9", 1)

# em seguida realizamos as operações
print("nome: ", ana.nome)
print("nacionalidade: ", ana.nacionalidade)
print("idade: ", ana.idade)
print(ana.descricao())
print(ana.fala("olá"))
print("--------------------------")
print("nome: ", b9.nome)
print("nacionalidade: ", b9.nacionalidade)
print("idade: ", b9.idade)
print("fabricante: ", b9.fabricante)
print("tipo: ", b9.tipo)
print(b9.correr())
```

O resultado será:

```python
nome:  ana
nacionalidade:  brasileiro
idade:  33
ana tem: 33 anos de idade
ana diz: olá
--------------------------
nome:  robo b9
nacionalidade:  brasileiro
idade:  1
fabricante:  tecnologia nacional
tipo:  robo humanoide
Humanoide pode correr
```

[Voltar ao sumário](#sumário)<br>



## 21.3. Encapsulação

Exemplo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Pessoa:

    def __init__(self):
        self.__salarioBase = 1300

    def informaSalario(self):
        print("Salario base: {}".format(self.__salarioBase))

    def setMaxPrice(self, base):
        self.__salarioBase = base

p = Pessoa()
p.informaSalario()


# em seguida realizamos as operações:

# muda salario base
p.__salarioBase = 2000
p.informaSalario()

# using setter function
p.setMaxPrice(3000)
p.informaSalario()
```

O resultado será:

```python
Salario base: 1300
Salario base: 1300
Salario base: 3000
```

[Voltar ao sumário](#sumário)<br>




## 21.4. Polimorfismo

Exemplo:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
class Veiculo:
    # method to render a shape
    def chamar(self):
        print("Chamando o Veiculo.")

class SUV(Veiculo):
    # renders SUV
    def chamar(self):
        print("Chamando o SUV.")

class Sedan(Veiculo):
    # renders Sedan
    def chamar(self):
        print("Chamando o Sedan.")

# em seguida realizamos as operações:
veiculo1 = Veiculo()
veiculo1.chamar()    

# create an object of SUV
suv1 = SUV()
suv1.chamar()

# create an object of Sedan
sedan1 = Sedan()
sedan1.chamar()
```

O resultado será:

```python
Chamando o Veiculo.
Chamando o SUV.
Chamando o Sedan.
```

[Voltar ao sumário](#sumário)<br>



---
# C - Banco MySQL (MariaDB)

# 22. Python com MySQL


Para instalar o conector mysql no python use o comando no promt:
python -m pip install mysql-connector-python


[Voltar ao sumário](#sumário)<br>





## 22.1. SQL create database

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password=""
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações
dbcursor.execute("SHOW DATABASES")
for x in dbcursor:
  print(x)

print("Cria o banco de dados: escola")
dbcursor.execute("CREATE DATABASE escola")
```

O resultado será:

```python
('information_schema',)
('mysql',)
('performance_schema',)
('sys',)
Cria o banco de dados: escola
```

[Voltar ao sumário](#sumário)<br>





## 22.2. SQL create table

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password="",
  database="escola"
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações
dbcursor.execute("SHOW DATABASES")
for x in dbcursor:
  print(x)
print("Cria a tabela: alunos")
dbcursor.execute("CREATE TABLE alunos (nome VARCHAR(50), idade VARCHAR(2))")
```

O resultado será:

```python
('escola',)
('information_schema',)
('mysql',)
('performance_schema',)
('sys',)
Cria a tabela: alunos
```

[Voltar ao sumário](#sumário)<br>




## 22.3. SQL Insert, Delete, Update

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password="",
  database="escola"
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações
sql1 = "INSERT INTO alunos (nome, idade) VALUES (%s, %s)"
val1 = ("pedro", "30")
val2 = ("ana", "40")
val3 = ("joao", "35")
dbcursor.execute(sql1, val1)
bancodedados.commit()
print("--- insert ---------------")
print(dbcursor.rowcount, "registro inserido", val1)
dbcursor.execute(sql1, val2)
bancodedados.commit()
print(dbcursor.rowcount, "registro inserido", val2)
dbcursor.execute(sql1, val3)
bancodedados.commit()
print(dbcursor.rowcount, "registro inserido", val3)

print("--- delete ---------------")
sql2 = "DELETE FROM alunos WHERE nome = 'joao'"
dbcursor.execute(sql2)
bancodedados.commit()
print(dbcursor.rowcount, "registro deletado", val3)

print("--- update ---------------")
sql3 = "UPDATE alunos SET idade = '41' WHERE idade = '40'"
dbcursor.execute(sql3)
bancodedados.commit()
print(dbcursor.rowcount, "registro atualizado")
```

O resultado será:

```python
--- insert ---------------
1 registro inserido ('pedro', '30')
1 registro inserido ('ana', '40')
1 registro inserido ('joao', '35')
--- delete ---------------
1 registro deletado ('joao', '35')
--- update ---------------
1 registro atualizado
```

[Voltar ao sumário](#sumário)<br>



## 22.4. SQL Select

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password="",
  database="escola"
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações

print("--- select ---------------")
dbcursor.execute("SELECT * FROM alunos")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)
```

O resultado será:

```python
--- select ---------------
('pedro', '30')
('ana', '41')
('alvaro', '37')
('fernando', '26')
```

[Voltar ao sumário](#sumário)<br>






## 22.5. Sum, Max, Min, Avg, Count

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password="",
  database="escola"
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações

print("--- soma ---------------")
dbcursor.execute("SELECT SUM(idade) AS TotalIdade FROM alunos;")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)
  
print("--- max ---------------")
dbcursor.execute("SELECT MAX(idade) AS MaxIdade FROM alunos;")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)
  
print("--- min ---------------")
dbcursor.execute("SELECT MIN(idade) AS MinIdade FROM alunos;")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)

print("--- media ---------------")
dbcursor.execute("SELECT AVG(idade) AS mediaIdade FROM alunos;")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)
  
print("--- countar ---------------")
dbcursor.execute("SELECT COUNT(idade) AS ontagemIdade FROM alunos;")
resultado = dbcursor.fetchall()
for x in resultado:
  print(x)
```

O resultado será:

```python
--- soma ---------------
(134.0,)
--- max ---------------
('41',)
--- min ---------------
('26',)
--- media ---------------
(33.5,)
--- contar ---------------
(4,)
```
[Voltar ao sumário](#sumário)<br>







## 22.6. SQL drop table e drop database

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import mysql.connector
bancodedados = mysql.connector.connect(
  host="localhost",
  user="root",
  password="",
  database="escola"
)
dbcursor = bancodedados.cursor()

# em seguida realizamos as operações
dbcursor = bancodedados.cursor()
sql1 = "DROP TABLE alunos"
dbcursor.execute(sql1)
print("tabela deletada: alunos")
print("----------------------------")
sql2 = "DROP DATABASE escola"
dbcursor.execute(sql2)
print("banco de dados deletado: escola")
```

O resultado será:

```
tabela deletada: alunos
----------------------------
banco de dados deletado: escola
```


```
Site para treinamento com SQL:
https://www.db-fiddle.com/
```

[Voltar ao sumário](#sumário)<br>








---
# D - Banco MongoDB

# 23. Python com MongoDB


```python
import pymongo

clienteMongo = pymongo.MongoClient("mongodb://localhost:27017/")
db1 = clienteMongo["aula10b"]
col1 = db1["alunos3"]

x = col1.find_one()

# imprimir o primeiro documento
print(x)

# imprimir todos os documentos
for col1 in col1.find():
    print(col1)
```

O resultado será:

```
{'_id': ObjectId('653041528a0a55c981579857'), 'nome': 'bill', 'nota': 7}
-------------------
{'_id': ObjectId('653041528a0a55c981579857'), 'nome': 'bill', 'nota': 7}
{'_id': ObjectId('653041618a0a55c981579858'), 'nome': 'maria', 'nota': 93}
{'_id': ObjectId('653049258a0a55c98157985a'), 'nome': 'daniel', 'nota': 6}
{'_id': ObjectId('653049258a0a55c98157985b'), 'nome': 'mauricio', 'nota': 8}
{'_id': ObjectId('653049258a0a55c98157985c'), 'nome': 'joao', 'nota': 7}
```


[Voltar ao sumário](#sumário)<br>




---
# E - Plotagem de gráficos

# 24. Plot e gráficos

```python
Em desenvolvimento
```
## 24.1. Gráfico com matplotlib

```python
import matplotlib.pyplot as plt1
import numpy as npy

xpoints = npy.array([1, 5, 8, 10])
ypoints = npy.array([3, 8, 10, 15])

plt1.plot(xpoints, ypoints)
plt1.show()
```

Exemplo com linhas:

```python
import matplotlib.pyplot as plt1
import numpy as npy

ypoints = npy.array([2, 7, 5, 11])

plt1.xlabel("Eixo X")
plt.ylabel("Eixo y")

plt1.plot(ypoints, linestyle = 'dotted')
plt1.grid()
plt1.show()
```

Exemplo com barras:

```python
import matplotlib.pyplot as plt1
import numpy as npy

x = npy.array(["X", "Y", "Z", "W"])
y = npy.array([5, 9, 4, 11])

plt1.bar(x,y)
plt1.grid()
plt1.show()
```

[Voltar ao sumário](#sumário)<br>




## 24.2. Gráfico pizza

```python
import matplotlib.pyplot as plt1
  
# definição de classes ou categorias da pizza
classes = ['classe1', 'classe2', 'classe3', 'classe4']
  
# valores das classes
fatias = [5, 5, 3, 9]
  
# cores de cada classe
cores = ['r', 'y', 'g', 'b']
  
# montando a pizza
plt1.pie(fatias, labels = classes, colors=cores, 
        startangle=90, shadow = True, explode = (0, 0, 0.1, 0),
        radius = 1.2, autopct = '%1.1f%%')
  
# plotando a legenda
plt1.legend()
  
# mostrando a pizza
plt1.show()
```

[Voltar ao sumário](#sumário)<br>



### 24.2.1. Gráfico de pizza com matplotlib

```
Em desenvolvimento
```


```python
# -*- coding: utf-8 -*-
import pandas as pds
import seaborn as sbn
import matplotlib.pyplot as plt1

filmes = pds.read_csv("tmdb_5000_movies.csv")
# foi utilizado o arquivo: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?resource=download

#sbn.catplot(x="original_language", kind="count", data=filmes)

filmes_por_categoria = filmes["original_language"].value_counts().to_frame()
filmes_por_categoria = filmes["original_language"].value_counts().to_frame().reset_index()
filmes_por_categoria.columns = ["original_language", "total"]
print(filmes_por_categoria.head())

plt1.pie(filmes_por_categoria["total"], labels = filmes_por_categoria["original_language"])
```

[Voltar ao sumário](#sumário)<br>



## 24.3. Grafico com numpy

np.mean, função mean do numpy é usada para calcular a média aritmética ou média dos elementos da matriz junto com o eixo especificado ou eixo múltiplo.

```python
import numpy as npy
import matplotlib.pyplot as plt1

dados = {'Empresa0': 109.50,
        'Empresa1': 104.59,
        'Empresa2': 114.71,
        'Empresa3': 113.43,
        'Empresa4': 100.30,
        'Empresa5': 102.54,
        'Empresa6': 137.96,
        'Empresa6': 123.38,
        'Empresa7': 135.99,
        'Empresa8': 123.60}
group_dados = list(dados.values())
group_nomes = list(dados.keys())
group_mean = npy.mean(group_dados)

fig, ax = plt1.subplots()
ax.barh(group_nomes, group_dados)
```

[Voltar ao sumário](#sumário)<br>



## 24.4. Gráfico da distribuição normal

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import numpy
import matplotlib.pyplot as plt1

idade1 = [53,66,77,34,75,25,47,54,67,83,77]

# cria 1000 numeros aleatórios entre 1 e 5
idade2 = numpy.random.normal(1.0, 5.0, 1000)

# em seguida realizamos as operações
# criar um gráfico com os dados do vetor idade1
plt1.hist(idade1, 100)
plt1.show()
 
# cria um gráfico com os dados gerados aleatóriamente
plt1.hist(idade2, 100)
plt1.show()
```

[Voltar ao sumário](#sumário)<br>



## 24.5. Gráfico de dispersão

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import matplotlib.pyplot as plt

             # 1  2  3  4  5  6  7  8  9 10
velocidade  = [53,66,77,34,75,25,47,54,67,83]
idade       = [10,15,12,20, 8, 5,11,18,7,3]

# em seguida realizamos as operações
#           eixo-x eixo-y
plt.scatter(idade, velocidade)
plt.show()
```

[Voltar ao sumário](#sumário)<br>



## 24.6. Gráfico boxplot com seaborn

Definição: Seaborn...

```
Em desenvolvimento
```

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import pandas as pds
import seaborn as sbn

notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

print("-- mudar o título do cabeçalho ----------------------------")
notas.columns = ["usuario", "filme", "nota", "timestamp"]
print(notas.head())

#print("--- várias medidas ---")
#print(notas.nota.describe())

sbn.boxplot(notas.nota)
```

[Voltar ao sumário](#sumário)<br>




## 24.7. Gráfico de histograma

```python
# -*- coding: utf-8 -*-
import pandas as pds

notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

print("-- mudar o título do cabeçalho ----------------------------")
notas.columns = ["usuario", "filme", "nota", "timestamp"]
print(notas.head())

print("--- mostrar uma coluna 2 (forma1) ---------------------------")
print(notas["nota"])

print("--- mostras uma coluna 2 (forma2) ------------------")
print(notas.nota)

print("--- mostras uma coluna 2 (forma3) ------------------")
print(notas.nota.head)

print("--- mostrar um gráfico do tipo histograma com os valores de nota")
print(notas.nota.plot(kind='hist'))

```

[Voltar ao sumário](#sumário)<br>







## 24.8. Gráfico de histogramas com Seabor e KDE

```
KDE (kernel density estimates)
Em desenvolvimento
```


```python
# -*- coding: utf-8 -*-
import pandas as pds
import seaborn as sbn

filmes = pds.read_csv("movies.csv")
notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

print("-- mudar o título do cabeçalho ----------------------------")
#filmes.columns = ["id_filme", "titulo", "genero"]
#notas.columns = ["usuario", "id_filme", "nota", "timestamp"]
print(filmes.head())
print(notas.head())

print("--- exemplo2: media por grupos de filmes usando a coluna nota (rating) ---")
medias_por_filme = notas.groupby("movieId").mean().rating
print(medias_por_filme.head)

#print("--- histograma de médias por filmes ---")
medias_por_filme.plot(kind="hist")

print("--- histograma de médias por filmes usando seaborn ---")
#sbn.boxplot(medias_por_filme)
sbn.displot(medias_por_filme)

# KDE kernel density estimates (KDEs)
print("--- alterando a quantidade de colunas no gráfico(bins)")
sbn.displot(medias_por_filme, bins=15, kde=True)

print("--- desta forma o seaborn decide sozinho a quantidade de colunas")
sbn.displot(medias_por_filme, kde=True)
```


[Voltar ao sumário](#sumário)<br>




## 24.9. Gráfico com Matplotlib, KDE, Seaborn, Pyplot


```
Em desenvolvimento
```


```python
# -*- coding: utf-8 -*-
import pandas as pds
import seaborn as sbn
import matplotlib.pyplot as plt1

filmes = pds.read_csv("movies.csv")
notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

#print("--- exemplo2: media por grupos de filmes usando a coluna nota (rating) ---")
medias_por_filme = notas.groupby("movieId").mean().rating
#print(medias_por_filme.head)

# --- gráfico 1: histograma de médias por filmes ---
medias_por_filme.plot(kind="hist")

# --- gráfico 2: usando KDE kernel density estimates (KDEs)
sbn.displot(medias_por_filme, bins=15, kde=True)

# --- gráfico 3: desta forma o seaborn decide sozinho a quantidade de colunas
sbn.displot(medias_por_filme, kde=True)

# --- gráfico 4: usando matplotlib
plt1.hist(medias_por_filme)
plt1.title("titulo de gráfico aqui !")
```


[Voltar ao sumário](#sumário)<br>




### 24.9.1. Gráfico de categorias com Seaborn e parâmetro kind

```
Em desenvolvimento
```


```python
# -*- coding: utf-8 -*-
import pandas as pds
import seaborn as sbn

# gráfico de barras para as categorias usando seaborn kind
filmes = pds.read_csv("tmdb_5000_movies.csv")
sbn.catplot(x="original_language", kind="count", data=filmes)
```

[Voltar ao sumário](#sumário)<br>





---
# F - Estatísticas

# 25. Exemplos diversos com estatísticas

Exemplo:

```python
Em desenvolvimento
```

## 25.1 Media, mediana, moda e desvio padrão

A média (mean) de um conjunto de dados é encontrada somando-se todos os números do conjunto de dados e então dividindo o resultado pelo número de valores do conjunto.<br>
A mediana (median) é o valor do meio quando o conjunto de dados está ordenado do menor para o maior. <br>
A moda (mode) é o número que aparece mais vezes em um conjunto de dados.<br>
Desvio padrão é o grau de dispersão de um conjunto de elementos.<br>

[Fonte: https://pt.khanacademy.org/math/ap-statistics/summarizing-quantitative-data-ap/measuring-center-quantitative/v/statistics-intro-mean-median-and-mode#:~:text=A%20m%C3%A9dia%20de%20um%20conjunto,em%20um%20conjunto%20de%20dados]

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import numpy

idade = [53,66,77,34,75,25,47,54,67,83,77]
x = numpy.mean(idade)
y = numpy.median(idade)
from scipy import stats
w = stats.mode(idade, axis=None, keepdims=False)
y = numpy.std(idade)

# em seguida realizamos as operações
print("media: ", x)
print("mediana: ", y)
print("moda: ", w)
print("desvio padrão: ", y)
```

O resultado será:

```
media:  59.81818181818182
mediana:  18.019273428083416
moda:  ModeResult(mode=77, count=2)
desvio padrão:  18.019273428083416
```

[Voltar ao sumário](#sumário)<br>




## 25.2. Percentil e porcentagem

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import numpy

idade = [53,66,77,34,75,25,47,54,67,83,77]
x = numpy.percentile(idade, 50)

def qual_a_porcentagem(numero1, numero2):
    return (numero1 / numero2) * 100

# em seguida realizamos as operações
print("idade = [53,66,77,34,75,25,47,54,67,83,77]")
print("o percentil das idades é: ", x)
print("--------------------------------")
print("Exemplo de porcentagem")
print("25% de 100 é: ", qual_a_porcentagem(25, 100))  
print("15% de 93 é: ", qual_a_porcentagem(15, 93))  
print("arredondando: ",  round(qual_a_porcentagem(15, 93), 2)) 
```

O resultado será:

```
idade = [53,66,77,34,75,25,47,54,67,83,77]
o percentil das idades é:  66.0
--------------------------------
Exemplo de porcentagem
25% de 100 é:  25.0
15% de 93 é:  16.129032258064516
arredondando:  16.13
```

[Voltar ao sumário](#sumário)<br>



## 25.3. Regressão

Definição1:

```
Em desenvolvimento
```

Definição2:

[Voltar ao sumário](#sumário)<br>



### 25.3.1. Regressão linear

Definição: 

```
Em desenvolvimento
```

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import matplotlib.pyplot as plt1
from scipy import stats

             # 1  2  3  4  5  6  7  8  9 10
velocidade  = [90,93,80,75,79,83,89,71,95,85]
idade       = [10,9,12,11, 11, 11,11,12,7,9]


slope, intercept, r, p, std_err = stats.linregress(velocidade, idade)

def funcao1(velocidade):
  return slope * velocidade + intercept

modelo1 = list(map(funcao1, velocidade))

# em seguida realizamos as operações
#           eixo-x eixo-y
plt1.scatter(velocidade, idade)
plt1.plot(velocidade, modelo1)
plt1.show()
```

Observações:
https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.linregress.html

Slope represente os passos em uma linha. slope: inclinação da linha de regressão.
Interceptar : interceptar a linha de regressão.
Valor-r: coeficiente de correlação.
Valor p : valor p bilateral para um teste de hipótese cuja hipótese nula é que a inclinação é zero.
Stderr : Erro padrão da estimativa.

Predizer a velocidade para um carro com 10 anos:

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
from scipy import stats

             # 1  2  3  4  5  6  7  8  9 10
velocidade  = [90,93,80,75,79,83,89,71,95,85]
idade       = [10,9,12,11,11,11,11,12,7,9]

slope, intercept, r, p, std_err = stats.linregress(idade, velocidade)

def funcao1(idade):
  return slope * idade + intercept

# em seguida realizamos as operações
velocidade2 = funcao1(10)
print(velocidade2)
```

O resultado será:

```python
85.18099547511312
```

[Voltar ao sumário](#sumário)<br>




### 25.3.2. Regressão polinomial

Definição:


```
Em desenvolvimento
```

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
import numpy
import matplotlib.pyplot as plt1

hora = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]             
velocidade  = [90,93,65,65,63,65,67,71,72,71,78,67,70,80,80,64,78,75,90,100]
       
modelo1 = numpy.poly1d(numpy.polyfit(hora, velocidade, 3))
linha1 = numpy.linspace(1, 22, 100)

# em seguida realizamos as operações
plt1.scatter(hora, velocidade)
plt1.plot(linha1, modelo1(linha1))
plt1.show()
```

[Voltar ao sumário](#sumário)<br>




### 25.4. Contagem de valores, média e mediana com pandas dataframe

```python
# -*- coding: utf-8 -*-
import pandas as pds

notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

print("--- primeiras linhas ---------------------------")
print(notas.head())

print("--- formato ---------------------------")
print(notas.shape)

print("-- mudar o título do cabeçalho ----------------------------")
notas.columns = ["usuario", "filme", "nota", "timestamp"]
print(notas.head())

print("--- mostrar uma coluna ---------------------------")
print(notas["nota"])

print("--- mostrar os valores unicos de uma coluna ----------")
print(notas["nota"].unique())

print("--- contar a quantidade de valores na coluna -----------")
print(notas["nota"].value_counts())

print("--- média de todos valores da coluna  -----------")
print(notas["nota"].mean())

print("--- médiana de todos valores da coluna  -----------")
print(notas["nota"].median())

print("--- ver os valores de uma coluna ------------------")
print(notas.nota)

```

O resultado será:

```
--- primeiras linhas ---------------------------
   userId  movieId  rating  timestamp
0       1        1     4.0  964982703
1       1        3     4.0  964981247
2       1        6     4.0  964982224
3       1       47     5.0  964983815
4       1       50     5.0  964982931
--- formato ---------------------------
(100836, 4)
-- mudar o título do cabeçalho ----------------------------
   usuario  filme  nota  timestamp
0        1      1   4.0  964982703
1        1      3   4.0  964981247
2        1      6   4.0  964982224
3        1     47   5.0  964983815
4        1     50   5.0  964982931
--- mostrar uma coluna ---------------------------
0         4.0
1         4.0
2         4.0
3         5.0
4         5.0

100831    4.0
100832    5.0
100833    5.0
100834    5.0
100835    3.0
Name: nota, Length: 100836, dtype: float64
--- mostrar os valores unicos de uma coluna ----------
[4.  5.  3.  2.  1.  4.5 3.5 2.5 0.5 1.5]
--- contar a quantidade de valores na coluna -----------
4.0    26818
3.0    20047
5.0    13211
3.5    13136
4.5     8551
2.0     7551
2.5     5550
1.0     2811
1.5     1791
0.5     1370
Name: nota, dtype: int64
--- média de todos valores da coluna  -----------
3.501556983616962
--- médiana de todos valores da coluna  -----------
3.5
--- ver os valores de uma coluna ------------------
0         4.0
1         4.0
2         4.0
3         5.0
4         5.0

100831    4.0
100832    5.0
100833    5.0
100834    5.0
100835    3.0
Name: nota, Length: 100836, dtype: float64
```

[Voltar ao sumário](#sumário)<br>






### 25.5. Média, desvio padrão, mínimo, máximo. pandas dataframe

```python
# -*- coding: utf-8 -*-
import pandas as pds

notas = pds.read_csv("ratings.csv")
# foi utilizado o arquivo: https://grouplens.org/datasets/movielens/

print("-- mudar o título do cabeçalho ----------------------------")
notas.columns = ["usuario", "filme", "nota", "timestamp"]
print(notas.head())

print("--- várias medidas ---")
print(notas.nota.describe())

```

O resultado será:

```
-- mudar o título do cabeçalho ----------------------------
   usuario  filme  nota  timestamp
0        1      1   4.0  964982703
1        1      3   4.0  964981247
2        1      6   4.0  964982224
3        1     47   5.0  964983815
4        1     50   5.0  964982931
--- várias medidas ---
count    100836.000000
mean          3.501557
std           1.042529
min           0.500000
25%           3.000000
50%           3.500000
75%           4.000000
max           5.000000
Name: nota, dtype: float64
```

[Voltar ao sumário](#sumário)<br>




---
# G - GUI

# 26. GUI com Pyforms

Instalação do PyForms, via command prompt:<br>
pip install pyforms

```python
from tkinter import *
window = Tk()
window.title("tela1")
window.geometry('200x200')
lbl = Label(window, text="exemplo1")
lbl.grid(column=0, row=0)

def clicked():
    lbl.configure(text="exemplo2")

btn = Button(window, text="clique aqui", command=clicked)
btn.grid(column=1, row=0)
window.mainloop()
```


```
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>

---
# H - Analise de dados

## 27.1 Numpy


**Definição da Wikipedia:**

NumPy é uma biblioteca para a linguagem de programação Python, que suporta o processamentode grandes, multi-dimensionais arranjos e matrizes, juntamente com uma grande coleção de funções matemáticas de alto nível para operar sobre estas matrizes. O ancestral do NumPy, o Numeric, foi originalmente criado por Jim Hugunin com contribuições de vários outros desenvolvedores. Em 2005, Travis Oliphant criou o NumPy incorporando recursos do Numarray concorrente no Numeric, com extensas modificações. NumPy é um software de código aberto e tem muitos colaboradores.

Exemplos:


```python
import numpy as np
a = np.array([1,2,3,4,5])

vetor_array1 = np.array([0, 1, 2, 3, 4, 5, 6])

# Cria um array com zeros
np.zeros((3,4))

# Cria um array vazios
np.empty((3,2))

# Salva um array
np.save('array1.txt', a)

np.savez('array2.txt', a)

# Carregando do disco
np.load('array2.txt.npz')

# Salvando como txt
np.savetxt('array3.txt.npz', a, delimiter=",")

# Mostrando as dimensões de um array
print(vetor_array1.shape)

# Mostrando o tamanho do array
print(len(vetor_array1))

# Mostrando as dimensões do array
print(vetor_array1.ndim)

# Mostrando os elementos do array
print(vetor_array1.size)
```

### 27.1.1. Geração de números randômicos

```python
from numpy import random
x = random.randint(1000)
print(x)
```

### 27.1.2. Copy e View

```python
import numpy as np
vetor1 = np.array([1, 2, 3, 4, 5])
x = vetor1.copy()
y = vetor1.view()
vetor1[0] = 50
print(vetor1)
print(x)
print(y)
```

O resultado será:
```python
[50  2  3  4  5]
[1 2 3 4 5]
[50  2  3  4  5]
```

### 27.1.3. Join, Split e Sort

```python
import numpy as np

vetor1 = np.array([1, 2, 3])
vetor2 = np.array([4, 5, 6])

vetor = np.concatenate((vetor1, vetor2))
vetor3 = np.array_split(vetor, 3)
vetor2 = np.array([3, 2, 0, 1])

print(vetor1)
print(np.sort(vetor2))
print(vetor3)
```

O resultado será:
```python
[1 2 3]
[0 1 2 3]
[array([1, 2]), array([3, 4]), array([5, 6])]
```

[Voltar ao sumário](#sumário)<br>

## 27.2. Pandas

Pandas é um biblioteca que permite trabalhar com dados tabulares. O conjunto de dados tabulares é chamado de dataframe.

![https://pandas.pydata.org/docs/_images/01_table_dataframe.svg](https://pandas.pydata.org/docs/_images/01_table_dataframe.svg)

<br>
Fonte da figura: https://pandas.pydata.org/docs/_images/01_table_dataframe.svg<br>
<br>

Todos os vetores no exemplo a baixo devem ter a mesma quantidade de elementos. Já é aceito pela comunidade instanciar a biblioteca com o apelido de "pd".
Exemplo do uso da biblioteca pandas:

```python
import pandas as pd

df = pd.DataFrame(
    {
        "Nome": [
            "Ana",
            "Barbara",
            "Carlos",
            "Deb",
            "Eloisa",
            "Fabio"
                ],
        "Idade": [25, 26, 27, 45, 46, 48],
        "Sexo": ["F", "F", "M", "F", "F", "M"],
    }
)

print(df)
```

O resultado será:

```
      Nome  Idade Sexo
0      Ana     25    F
1  Barbara     26    F
2   Carlos     27    M
3      Deb     45    F
4   Eloisa     46    F
5    Fabio     48    M
```



# 3D

## 28.1 Matplotlib


```python
import matplotlib.pyplot as plt

from mpl_toolkits.mplot3d import axes3d

fig, axs = plt.subplots(1, 3, subplot_kw={'projection': '3d'})

# Get the test data
X, Y, Z = axes3d.get_test_data(0.05)

# Plot the data
for ax in axs:
    ax.plot_wireframe(X, Y, Z, rstride=10, cstride=10)

# Set the orthographic projection.
axs[0].set_proj_type('ortho')  # FOV = 0 deg
axs[0].set_title("'ortho'\nfocal_length = ∞", fontsize=10)

# Set the perspective projections
axs[1].set_proj_type('persp')  # FOV = 90 deg
axs[1].set_title("'persp'\nfocal_length = 1 (default)", fontsize=10)

axs[2].set_proj_type('persp', focal_length=0.2)  # FOV = 157.4 deg
axs[2].set_title("'persp'\nfocal_length = 0.2", fontsize=10)

plt.show()
```

<bt>
Fonte do exemplo acima: https://matplotlib.org/stable/gallery/mplot3d/projections.html<br>
<br>



<!--

## 27.3. Seaborn

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.4. Matplotlib

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.5. Scikitlearn

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.6. TensorFlow

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.7. Keras

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.8. Pytorch

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.9. Theano

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.10. MxNet

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.11. Café

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>


## 27.12. CNT

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.13. Pillow

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.14. OpenCV

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.15. ApacheSpark

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 27.16 Hadoop

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>


---
# Desenvolvimento web

## 28.1 Django

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 28.2. Flask


```python
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>

## 28.3. CherryPy

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 28.4. Pyramid

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 28.5. TurboGears

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 28.6. Falcon

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 28.7. Tornado


```python
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>


---
# Desenvolvimento de app

## 29.1. Kivy

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 29.2. BeeWare


```python
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>

## 29.3. Python-for-android

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

---
# Web scraping

## 30.1. urllib

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 30.2 requests

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>


---
# Interações com o site

## 31.1. Selenium

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>


## 31.2. Webbot

```python
Em desenvolvimento
```


[Voltar ao sumário](#sumário)<br>

## 31.3. Webcrawler

```python
Em desenvolvimento
```

## 31.4. Scrapy

```python
Em desenvolvimento
```

-->

[Voltar ao sumário](#sumário)<br>

---
# Outros materiais



# Lista de IDEs

| Ferramenta   |  URL |
| ------------ |  --- |
| Codeblocks   | https://www.codeblocks.org/ |
| Microsoft Visual Studio Community  | https://visualstudio.microsoft.com/pt-br/vs/community/|
| Spyder |  https://www.spyder-ide.org/ |
| QT designer  | https://www.qt.io/download |
| QT Creator  | https://build-system.fman.io/qt-designer-download |
| Code Lite | https://codelite.org/ |
| Eric Python IDE  | http://eric-ide.python-projects.org/index.html |
| Anaconda | https://www.anaconda.com/download |

Outras IDEs: https://en.wikipedia.org/wiki/Comparison_of_integrated_development_environments

[Voltar ao sumário](#sumário)<br>





---
# Lista de editores de códigos

| Ferramenta    | URL |
| ------------  | --- |
| Visual Studio Code  | https://code.visualstudio.com/ |
| Notepad++  | https://notepad-plus-plus.org/downloads/ |
| Pulsar  | https://github.com/pulsar-edit/pulsar |
| Light Table  | http://lighttable.com/ |
| Geany  | https://geany.org/ |

[Voltar ao sumário](#sumário)<br>




---
# Referências

| Descrição    | URL |
| ------------  | --- |
| Documentação da linguagem  | https://docs.python.org/3/ |
| Livro The Python Language Reference Manual | https://www.amazon.com.br/Python-Language-Reference-Manual/dp/1906966141 |
| Referência da linguagem | https://docs.python.org/3/reference/index.html |

https://www.devopsschool.com/blog/python-tutorials-difference-between-list-array-tuple-set-dict/

[Voltar ao sumário](#sumário)<br>






Lista de ferramentas: https://github.com/monteiro74/lista_de_ferramentas#5-IDEs




---
# Avisos, licença, observações, estatísticas


## Aviso
```
Este material esta recebendo atualizações frequentes. 
As informações aqui contidas podem ser alteradas sem aviso prévio.
```

## Licença
```
Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) 
https://creativecommons.org/licenses/by-nc-sa/4.0/
```

## Observação
```
Primeira postagem em: Junho/2023.
```


## Estatísticas





Histórico de atualizações nos repositórios do Prof. Monteiro:<br>
[![teste](https://github-readme-activity-graph.vercel.app/graph?username=monteiro74&theme=github-compact)](https://github.com/monteiro74/tutorial_python)

[![GitHub Streak](https://streak-stats.demolab.com/?user=monteiro74&theme=default)](https://git.io/streak-stats)

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=monteiro74)](https://github.com/monteiro74/github-readme-stats)

Pulse:<br>
https://github.com/monteiro74/tutorial_python/pulse<BR>


Histórico de frequência de código:<BR>
https://github.com/monteiro74/tutorial_python/graphs/code-frequency<BR>

Atividade de commits:<BR>
https://github.com/monteiro74/tutorial_python/graphs/commit-activity<BR>

Trafego:<BR>
https://github.com/monteiro74/tutorial_python/graphs/traffic<BR>

![stats](https://github-readme-stats.vercel.app/api?username=monteiro74&show=reviews,discussions_started,discussions_answered,prs_merged,prs_merged_percentage)

![stats](https://github-readme-stats.vercel.app/api?username=monteiro74&show_icons=true&theme=dark)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=monteiro74)](https://github.com/monteiro74/github-readme-stats)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=monteiro74&layout=donut-vertical)](https://github.com/monteiro74/github-readme-stats)

[Voltar ao sumário](#sumário)<br>

