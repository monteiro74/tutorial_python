# Tutorial sobre python


Objetivos: Pequenos exemplos para uso da linguagem python em sala de aula, em qualquer projetos de software. Exemplos que podem ser citados e comentados nas disciplinas que necessitam do apoio de uma linguagem de programação. Como prerequisito é necessário ter uma IDE instalada. Este material é extremamente resumido e supões que o leitor tem conhecimento básico de programação ou pelo menos português estruturado. (Esta é a versão: 2).<br>

## 📌 Finalidade e Público-Alvo

Este tutorial não se destina apenas ao ambiente acadêmico. Embora tenha sido desenvolvido inicialmente como material de apoio para disciplinas universitárias, **este conteúdo é igualmente valioso para profissionais da área de tecnologia** que desejam:

- Consultar rapidamente sintaxe e exemplos práticos de Python
- Revisar conceitos fundamentais e avançados da linguagem
- Utilizar como referência rápida em projetos profissionais
- Aprender ou relembrar bibliotecas específicas (MySQL, MongoDB, Matplotlib, Pandas, etc.)
- Ensinar Python para equipes ou colegas de trabalho

O material apresenta exemplos diretos e objetivos, facilitando o aprendizado prático tanto para estudantes quanto para desenvolvedores profissionais em busca de uma fonte de consulta eficiente.

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

# Sumário

- [Tutorial sobre python](#tutorial-sobre-python)
- [Sumário](#sumário)
- [1 - Conceitos e exemplos gerais da linguagem](#1---conceitos-e-exemplos-gerais-da-linguagem)
  - [1.1. Comando print](#11-comando-print)
  - [1.2. Comentário](#12-comentário)
    - [1.2.1. Codigo com acentos](#121-codigo-com-acentos)
  - [1.3. Operações matemáticas](#13-operações-matemáticas)
    - [1.3.1. Python com números](#131-python-com-números)
    - [1.3.2. Exponenciação](#132-exponenciação)
    - [1.3.3. Módulo](#133-módulo)
  - [1.4. Tipos de dados e variáveis](#14-tipos-de-dados-e-variáveis)
    - [1.4.1. Operações com strings](#141-operações-com-strings)
      - [1.4.1.1. Concatenando strings](#1411-concatenando-strings)
      - [1.4.1.2. Tamanho de uma string](#1412-tamanho-de-uma-string)
      - [1.4.1.3. Percorrer uma string](#1413-percorrer-uma-string)
      - [1.4.1.4. Selecionando partes da string](#1414-selecionando-partes-da-string)
      - [1.4.1.5. String em minúsculo, capitalize e maiúsculo](#1415-string-em-minúsculo-capitalize-e-maiúsculo)
      - [1.4.1.6. Função strip, split](#1416-função-strip-split)
      - [1.4.1.7. Busca e substituição por substring](#1417-busca-e-substituição-por-substring)
      - [1.4.1.8. Formas de impressao de string](#1418-formas-de-impressao-de-string)
    - [1.4.2. Local e Global](#142-local-e-global)
  - [1.5. Operadores](#15-operadores)
  - [1.5.1. Operadores matemáticos](#151-operadores-matemáticos)
    - [1.5.2. Operadores relacionais](#152-operadores-relacionais)
    - [1.5.3. Operadores lógicos](#153-operadores-lógicos)
  - [1.6. Tratamento de exceções](#16-tratamento-de-exceções)
  - [1.7. Estruturas condicionais (controle de fluxo)](#17-estruturas-condicionais-controle-de-fluxo)
    - [1.7.1. Break](#171-break)
    - [1.7.2. Continue](#172-continue)
    - [1.7.3. Pass](#173-pass)
    - [1.7.4. Match e case](#174-match-e-case)
  - [1.8. Estruturas de repetição](#18-estruturas-de-repetição)
    - [1.8.1. Laço while](#181-laço-while)
      - [1.8.1.1. Laço while true](#1811-laço-while-true)
    - [1.8.2. Laço for](#182-laço-for)
    - [1.8.3. Laço for e range](#183-laço-for-e-range)
  - [1.9. Funções](#19-funções)
    - [1.9.1. Função recursiva](#191-função-recursiva)
    - [1.9.2. Documentação de função](#192-documentação-de-função)
  - [1.10. Arquivos](#110-arquivos)
    - [1.10.1. Funções read, readline e readlines](#1101-funções-read-readline-e-readlines)
    - [1.10.1.1. Função readlines](#11011-função-readlines)
      - [1.10.1.2. Função read](#11012-função-read)
    - [1.10.2. Criar arquivos](#1102-criar-arquivos)
  - [1.11. Listas](#111-listas)
    - [1.11.1. Acessando elementos individuais da lista](#1111-acessando-elementos-individuais-da-lista)
    - [1.11.2. Percorrer elementos de uma listas](#1112-percorrer-elementos-de-uma-listas)
    - [1.11.3. Tamanho de listas](#1113-tamanho-de-listas)
    - [1.11.4. Adicionando itens na lista](#1114-adicionando-itens-na-lista)
    - [1.11.5. Procurar um elemento na lista](#1115-procurar-um-elemento-na-lista)
    - [1.11.6. Subtraindo elementos de uma lista](#1116-subtraindo-elementos-de-uma-lista)
    - [1.11.7. Ordenando itens da lista, sort](#1117-ordenando-itens-da-lista-sort)
      - [1.11.7.1. Sort decrescente/decrescente](#11171-sort-decrescentedecrescente)
      - [1.11.7.2. Sort inverter itens](#11172-sort-inverter-itens)
    - [1.11.8. Ordenando itens da lista, sorted](#1118-ordenando-itens-da-lista-sorted)
    - [1.11.9. Pop](#1119-pop)
    - [1.11.10. Funções para tratamento de listas](#11110-funções-para-tratamento-de-listas)
    - [1.11.10.1. List comprehensions](#111101-list-comprehensions)
      - [1.11.10.2. Função Enumerate](#111102-função-enumerate)
      - [1.11.10.3. Função Map](#111103-função-map)
      - [1.11.10.4. Função Reduce](#111104-função-reduce)
      - [1.11.10.5. Função Zip](#111105-função-zip)
  - [1.12. Tuplas](#112-tuplas)
  - [1.13. Sets](#113-sets)
  - [1.14. Dicionários](#114-dicionários)
    - [1.14.1. Função items](#1141-função-items)
    - [1.14.2. Função values e keys](#1142-função-values-e-keys)
  - [1.15. Comparação List, Tuple, Set, Dictionary](#115-comparação-list-tuple-set-dictionary)
  - [1.16. Números aleatórios](#116-números-aleatórios)
  - [1.17. Arrays](#117-arrays)
  - [1.18. Módulos](#118-módulos)
  - [1.19. Input](#119-input)
  - [1.20. Standard Library](#120-standard-library)
- [2. Programação Orientada a Objetos](#2-programação-orientada-a-objetos)
  - [2.1. Criando classes](#21-criando-classes)
    - [2.1.1. Instanciando objetos, atribuindo valores](#211-instanciando-objetos-atribuindo-valores)
  - [2.2. Sub classes e herança](#22-sub-classes-e-herança)
  - [2.3. Encapsulação](#23-encapsulação)
  - [2.4. Polimorfismo](#24-polimorfismo)
- [3 - Banco MySQL (MariaDB)](#3---banco-mysql-mariadb)
  - [3.1. Python com MySQL](#31-python-com-mysql)
  - [3.2. SQL create database](#32-sql-create-database)
  - [3.3. SQL create table](#33-sql-create-table)
  - [3.4. SQL Insert, Delete, Update](#34-sql-insert-delete-update)
  - [3.5. SQL Select](#35-sql-select)
  - [3.6. Sum, Max, Min, Avg, Count](#36-sum-max-min-avg-count)
  - [3.7. SQL drop table e drop database](#37-sql-drop-table-e-drop-database)
- [4. - Banco MongoDB](#4---banco-mongodb)
  - [4.1. Python com MongoDB](#41-python-com-mongodb)
- [5 - Plotagem de gráficos](#5---plotagem-de-gráficos)
  - [5.1. Plot e gráficos](#51-plot-e-gráficos)
  - [5.2. Gráfico com matplotlib](#52-gráfico-com-matplotlib)
  - [5.3. Gráfico pizza](#53-gráfico-pizza)
    - [5.3.1. Gráfico de pizza com matplotlib](#531-gráfico-de-pizza-com-matplotlib)
  - [5.4. Grafico com numpy](#54-grafico-com-numpy)
  - [5.5. Gráfico da distribuição normal](#55-gráfico-da-distribuição-normal)
  - [5.6. Gráfico de dispersão](#56-gráfico-de-dispersão)
  - [5.7. Gráfico boxplot com seaborn](#57-gráfico-boxplot-com-seaborn)
  - [5.8. Gráfico de histograma](#58-gráfico-de-histograma)
  - [5.9. Gráfico de histogramas com Seabor e KDE](#59-gráfico-de-histogramas-com-seabor-e-kde)
  - [5.10. Gráfico com Matplotlib, KDE, Seaborn, Pyplot](#510-gráfico-com-matplotlib-kde-seaborn-pyplot)
    - [5.10.1. Gráfico de categorias com Seaborn e parâmetro kind](#5101-gráfico-de-categorias-com-seaborn-e-parâmetro-kind)
- [6. Estatísticas](#6-estatísticas)
  - [6.1. Exemplos diversos com estatísticas](#61-exemplos-diversos-com-estatísticas)
  - [6.2 Media, mediana, moda e desvio padrão](#62-media-mediana-moda-e-desvio-padrão)
  - [6.3. Percentil e porcentagem](#63-percentil-e-porcentagem)
  - [6.4. Regressão](#64-regressão)
    - [6.4.1. Regressão linear](#641-regressão-linear)
    - [6.4.2. Regressão polinomial](#642-regressão-polinomial)
  - [6.5. Contagem de valores, média e mediana com pandas dataframe](#65-contagem-de-valores-média-e-mediana-com-pandas-dataframe)
  - [6.6. Média, desvio padrão, mínimo, máximo. pandas dataframe](#66-média-desvio-padrão-mínimo-máximo-pandas-dataframe)
- [7. GUI](#7-gui)
  - [7.1. GUI com Pyforms](#71-gui-com-pyforms)
- [8. Analise de dados](#8-analise-de-dados)
  - [8.1 Numpy](#81-numpy)
    - [8.1.1. Geração de números randômicos](#811-geração-de-números-randômicos)
    - [8.1.2. Copy e View](#812-copy-e-view)
    - [8.1.3. Join, Split e Sort](#813-join-split-e-sort)
  - [8.2. Pandas](#82-pandas)
    - [8.2.1. Importar arquivo csv e estatísticas básicas](#821-importar-arquivo-csv-e-estatísticas-básicas)
- [9. 3D](#9-3d)
  - [9.1 Matplotlib](#91-matplotlib)
  - [9.2. Outro exemplo com Matplotlib](#92-outro-exemplo-com-matplotlib)
  - [9.3. Axes3D](#93-axes3d)
- [Lista de IDEs](#lista-de-ides)
- [Lista de editores de códigos](#lista-de-editores-de-códigos)
- [Referências](#referências)
- [Avisos, licença, observações, estatísticas](#avisos-licença-observações-estatísticas)
  - [Aviso](#aviso)
  - [Licença](#licença)
  - [Observação](#observação)
  - [Estatísticas](#estatísticas)
- [Como Contribuir](#como-contribuir)
- [Créditos](#créditos)
- [Como Citar Este Material](#como-citar-este-material)



---
# 1 - Conceitos e exemplos gerais da linguagem

## 1.1. Comando print

Impressão na tela, exemplo
```python
print("teste")
print("teste")
```

[Voltar ao sumário](#sumário)<br>



## 1.2. Comentário

Usando "#"

```python
# isto não é impresso
print("teste1")
""" isto não é impresso
print("teste2")
"""
print("teste3")
```

### 1.2.1. Codigo com acentos

```python
# -*- coding: utf-8 -*-
print("Olá mundo!")
```

[Voltar ao sumário](#sumário)<br>



## 1.3. Operações matemáticas

```python
print(2+2)
print(2-2)
print(2*2)
print(2/2)
```

### 1.3.1. Python com números

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



### 1.3.2. Exponenciação

```python
print(2**3)
```

### 1.3.3. Módulo

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



## 1.4. Tipos de dados e variáveis

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
4. o sinal de = é chamado de operador de atribuição, não é um sinal de igual !

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


### 1.4.1. Operações com strings

#### 1.4.1.1. Concatenando strings

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


#### 1.4.1.2. Tamanho de uma string

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


#### 1.4.1.3. Percorrer uma string

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



#### 1.4.1.4. Selecionando partes da string

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




#### 1.4.1.5. String em minúsculo, capitalize e maiúsculo

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



#### 1.4.1.6. Função strip, split

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


#### 1.4.1.7. Busca e substituição por substring

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


#### 1.4.1.8. Formas de impressao de string

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



### 1.4.2. Local e Global

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




## 1.5. Operadores

Recordando que = é um operador de atribuição.

## 1.5.1. Operadores matemáticos

Revisão de alguns operadores..

| Operador     | Operação |
| ----------- | ----------- |
| +      | Soma      |
| -  | Subtração        |
| * | Multiplicação |
| / | Divisão |
| ** | Exponenciação |
| % | Módulo |

### 1.5.2. Operadores relacionais

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


### 1.5.3. Operadores lógicos

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




## 1.6. Tratamento de exceções

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




## 1.7. Estruturas condicionais (controle de fluxo)

Também chamados de comandos estruturais.
Servem para realizar avaliações ou testes entre variáveis.

Depois de uma condição existe um bloco de código criado com uma tabulação.

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

### 1.7.1. Break


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



### 1.7.2. Continue

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




### 1.7.3. Pass

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




### 1.7.4. Match e case

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


## 1.8. Estruturas de repetição

Também são chamados de laços de repetição ou iteradores. Iterar é repetir. Desta forma um bloco (ou várias linhas de código) serão repetidas até que uma condição seja satisfeita.<br>

### 1.8.1. Laço while

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




#### 1.8.1.1. Laço while true

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


### 1.8.2. Laço for

Este laço usado para percorrer uma estrutura de dados, como uma lista, por exemplo:

```python
# declarações/atribuições
primeira_lista = [1,2,3,"ana","bob",True,5.66,0]

# em seguida realizamos as operações
for i in primeira_lista:
    print(i)
```

O resultado acima será:
```python
1
2
3
ana
bob
True
5.66
0
```

[Voltar ao sumário](#sumário)<br>



### 1.8.3. Laço for e range

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



## 1.9. Funções

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

### 1.9.1. Função recursiva

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


### 1.9.2. Documentação de função


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



## 1.10. Arquivos

O python pode manipular arquivos. Para abrir um arquivo é utilizada a função open. Os modos de trabalho com arquivos são: <br>


|Modo|	Descrição|
| --- | --- |
| r	| Abre o arquivo para leitura, é o default |
| w	| Abre o arquivo para leitura; criar um arquivo se o arquivo não existe ou troca o arquivo se existe.|
| x	| Abra um arquivo para criação exclusiva. Se o arquivo já existir, a operação falhará |
| a | Abra um arquivo para anexar no final do arquivo sem truncá-lo. Cria um novo arquivo se ele não existir. |
| t | Abre o arquivo em modo texto (default) |
| b | Abre um arquivo em modo binário. |



### 1.10.1. Funções read, readline e readlines

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

### 1.10.1.1. Função readlines

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

#### 1.10.1.2. Função read

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



### 1.10.2. Criar arquivos

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





## 1.11. Listas

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



### 1.11.1. Acessando elementos individuais da lista

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



### 1.11.2. Percorrer elementos de uma listas

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



### 1.11.3. Tamanho de listas

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

### 1.11.4. Adicionando itens na lista


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


### 1.11.5. Procurar um elemento na lista

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

### 1.11.6. Subtraindo elementos de uma lista

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



### 1.11.7. Ordenando itens da lista, sort

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



#### 1.11.7.1. Sort decrescente/decrescente

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

#### 1.11.7.2. Sort inverter itens


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

### 1.11.8. Ordenando itens da lista, sorted

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



### 1.11.9. Pop

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
### 1.11.10. Funções para tratamento de listas

Exemplo no uso de funções para tratamento de listas:

### 1.11.10.1. List comprehensions

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



#### 1.11.10.2. Função Enumerate

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
    print(indice, lista1[indice])
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






#### 1.11.10.3. Função Map

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






#### 1.11.10.4. Função Reduce

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




#### 1.11.10.5. Função Zip

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




## 1.12. Tuplas

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


## 1.13. Sets

Com os conjuntos é possível armazenar multiplos valores em uma única variável. Os conjuntos não podem ser ordenados.

```python
# -*- coding: utf-8 -*-
# declarações/atribuições
set1 = {"banana", "abacate", "melancia"}

# em seguida realizamos as operações
print(set1)
```

```python
{'banana', 'abacate', 'melancia'}
```

[Voltar ao sumário](#sumário)<br>


## 1.14. Dicionários

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
print("--- imprime os valores ---")
for chaveD in declaracoes1:
    print(declaracoes1[chaveD])
print("--- imprime chave e valores ---")
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
--- imprime os valores ---
ANA
BOB
CARLOS
DANIEL
--- imprime chave e valores ---
A:ANA
B:BOB
C:CARLOS
D:DANIEL
```

[Voltar ao sumário](#sumário)<br>



### 1.14.1. Função items

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




### 1.14.2. Função values e keys

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



## 1.15. Comparação List, Tuple, Set, Dictionary

| List | Tuple | Dictionary | Set
| --- | --- | --- | --- |
| Permite itens duplicados | Permite itens duplicados | Sem duplicados | Sem duplicados |
| Mutável | Não mutável | Mutável, indexável | Não pode ser mudada, mas pode ser adicionada, não indexada|
| Ordenada | Ordenada | Não ordenada | Não ordenada |
| [] ou list() | () ou tuple() | {}* ou set() | {} ou dict()|

Fonte: https://www.devopsschool.com/blog/python-tutorials-difference-between-list-array-tuple-set-dict/




## 1.16. Números aleatórios


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




## 1.17. Arrays

Python não tem suporte a arrays (matrizes), veja listas.

[Voltar ao sumário](#sumário)<br>




## 1.18. Módulos

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








## 1.19. Input


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



## 1.20. Standard Library

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
# 2. Programação Orientada a Objetos

## 2.1. Criando classes

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



### 2.1.1. Instanciando objetos, atribuindo valores

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



## 2.2. Sub classes e herança

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



## 2.3. Encapsulação

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




## 2.4. Polimorfismo

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
# 3 - Banco MySQL (MariaDB)

## 3.1. Python com MySQL


Para instalar o conector mysql no python use o comando no promt:
python -m pip install mysql-connector-python


[Voltar ao sumário](#sumário)<br>





## 3.2. SQL create database

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





## 3.3. SQL create table

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




## 3.4. SQL Insert, Delete, Update

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



## 3.5. SQL Select

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






## 3.6. Sum, Max, Min, Avg, Count

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
  
print("--- contar ---------------")
dbcursor.execute("SELECT COUNT(idade) AS contagemIdade FROM alunos;")
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







## 3.7. SQL drop table e drop database

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
# 4. - Banco MongoDB

## 4.1. Python com MongoDB


```python
import pymongo

clienteMongo = pymongo.MongoClient("mongodb://localhost:27017/")
db1 = clienteMongo["aula10b"]
col1 = db1["alunos3"]

x = col1.find_one()

# imprimir o primeiro documento
print(x)

# imprimir todos os documentos
for documento in col1.find():
    print(documento)
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
# 5 - Plotagem de gráficos

## 5.1. Plot e gráficos

```python
Em desenvolvimento
```
## 5.2. Gráfico com matplotlib

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




## 5.3. Gráfico pizza

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



### 5.3.1. Gráfico de pizza com matplotlib

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



## 5.4. Grafico com numpy

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
        'Empresa7': 135.99,
        'Empresa8': 123.60,
        'Empresa9': 123.38}
group_dados = list(dados.values())
group_nomes = list(dados.keys())
group_mean = npy.mean(group_dados)

fig, ax = plt1.subplots()
ax.barh(group_nomes, group_dados)
```

[Voltar ao sumário](#sumário)<br>



## 5.5. Gráfico da distribuição normal

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



## 5.6. Gráfico de dispersão

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



## 5.7. Gráfico boxplot com seaborn

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




## 5.8. Gráfico de histograma

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

print("--- mostra uma coluna 2 (forma2) ------------------")
print(notas.nota)

print("--- mostra uma coluna 2 (forma3) ------------------")
print(notas.nota.head)

print("--- mostrar um gráfico do tipo histograma com os valores de nota")
print(notas.nota.plot(kind='hist'))

```

[Voltar ao sumário](#sumário)<br>




## 5.9. Gráfico de histogramas com Seabor e KDE

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




## 5.10. Gráfico com Matplotlib, KDE, Seaborn, Pyplot


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



### 5.10.1. Gráfico de categorias com Seaborn e parâmetro kind

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
# 6. Estatísticas

## 6.1. Exemplos diversos com estatísticas

Exemplo:

```python
Em desenvolvimento
```

## 6.2 Media, mediana, moda e desvio padrão

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



## 6.3. Percentil e porcentagem

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


## 6.4. Regressão

Definição1:

```
Em desenvolvimento
```

Definição2:

[Voltar ao sumário](#sumário)<br>


### 6.4.1. Regressão linear

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


### 6.4.2. Regressão polinomial

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



## 6.5. Contagem de valores, média e mediana com pandas dataframe

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


## 6.6. Média, desvio padrão, mínimo, máximo. pandas dataframe

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
# 7. GUI

## 7.1. GUI com Pyforms

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

Outro exemplo:
```python
import tkinter as tk

class IMCCalculator:
    def __init__(self, root):
        self.root = root
        self.root.title('IMC Calculator')
        self.root.geometry('300x250')
        
        self.peso_label = tk.Label(root, text='Peso:')
        self.peso_label.grid(row=0, column=0, padx=10, pady=10)

        self.peso_edit = tk.Entry(root)
        self.peso_edit.grid(row=0, column=1, padx=10, pady=10)

        self.altura_label = tk.Label(root, text='Altura:')
        self.altura_label.grid(row=1, column=0, padx=10, pady=10)

        self.altura_edit = tk.Entry(root)
        self.altura_edit.grid(row=1, column=1, padx=10, pady=10)

        self.calcular_button = tk.Button(root, text='Calcular IMC', command=self.calcular_imc)
        self.calcular_button.grid(row=2, column=0, columnspan=2, pady=10)

        self.resultado_label = tk.Label(root, text='Resultado:')
        self.resultado_label.grid(row=3, column=0, columnspan=2, pady=10)

        self.sair_button = tk.Button(root, text='Sair', command=root.destroy)
        self.sair_button.grid(row=4, column=0, columnspan=2, pady=10)

    def calcular_imc(self):
        try:
            peso = float(self.peso_edit.get())
            altura = float(self.altura_edit.get())
            imc = peso / (altura ** 2)
            self.resultado_label.config(text=f'Resultado: {imc:.2f}')
        except ValueError:
            self.resultado_label.config(text='Por favor, insira valores válidos para peso e altura.')

if __name__ == "__main__":
    root = tk.Tk()
    app = IMCCalculator(root)
    root.mainloop()

```

```
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>

---
# 8. Analise de dados

## 8.1 Numpy


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

[Voltar ao sumário](#sumário)<br>

### 8.1.1. Geração de números randômicos

```python
from numpy import random
x = random.randint(1000)
print(x)
```

[Voltar ao sumário](#sumário)<br>


### 8.1.2. Copy e View

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

[Voltar ao sumário](#sumário)<br>

### 8.1.3. Join, Split e Sort

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

## 8.2. Pandas

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

Outro exemplo básico com pandas

```python
import pandas as pd

df123 = pd.DataFrame(
    {
        "Municipio": ["Sinop", "Caceres", "Sorriso"],
        "2023": ["45", "65", "78"],
        "2022": ["67", "60", "78"],
        "2021": ["73", "67", "87"],
        "2020": ["80", "45", "89"],
    }
)

print('--- imprime o dataframe ---')
print(df123)
print('--- imprime o head do dataframe ---')
print(df123.head())
print('--- imprime o tail do dataframe ---')
print(df123.tail())
print('--- imprime transpose do dataframe ---')
print(df123.T)
print('--- imprime uma coluna ---')
print(df123["2023"])
print('--- imprime duas linhas ---')
print(df123[0:2])
```

O resultado do código acima será:

```
--- imprime o dataframe ---
  Municipio 2023 2022 2021 2020
0     Sinop   45   67   73   80
1   Caceres   65   60   67   45
2   Sorriso   78   78   87   89
--- imprime o head do dataframe ---
  Municipio 2023 2022 2021 2020
0     Sinop   45   67   73   80
1   Caceres   65   60   67   45
2   Sorriso   78   78   87   89
--- imprime o tail do dataframe ---
  Municipio 2023 2022 2021 2020
0     Sinop   45   67   73   80
1   Caceres   65   60   67   45
2   Sorriso   78   78   87   89
--- imprime transpose do dataframe ---
               0        1        2
Municipio  Sinop  Caceres  Sorriso
2023          45       65       78
2022          67       60       78
2021          73       67       87
2020          80       45       89
--- imprime uma coluna ---
0    45
1    65
2    78
Name: 2023, dtype: object
--- imprime duas linhas ---
  Municipio 2023 2022 2021 2020
0     Sinop   45   67   73   80
1   Caceres   65   60   67   45
```

[Voltar ao sumário](#sumário)<br>

### 8.2.1. Importar arquivo csv e estatísticas básicas

Exemplo de importação de arquivo CSV e estatísticas básicas:

```python
import pandas as pd

df = pd.read_csv('D:\programacao\python\data2.csv')

print('--- listagem das linhas do arquivo --------')
print(df.to_string()) 


media1 = df['Pulse'].mean()
soma = df['Pulse'].sum()
max1 = df['Pulse'].max()
min1 = df['Pulse'].min()
countagem1 = df['Pulse'].count()
mediana1 = df['Pulse'].median() 
desvioPadrao1 = df['Pulse'].std() 
variancia1 = df['Pulse'].var()  

print("--- Estatísticas simples -----------------")
print('Media de Pulse: ' + str(media1))
print('Soma de Pulse: ' + str(soma))
print('Max de Pulse: ' + str(max1))
print('Min de Pulse: ' + str(min1))
print('Contagem de Pulse: ' + str(countagem1))
print('mediana de Pulse: ' + str(mediana1))
print('Desvio padrão de Pulse: ' + str(desvioPadrao1))
print('Variação de Pulse: ' + str(variancia1))
```

O resultado será:
```
--- listagem das linhas do arquivo --------
    Duration  Pulse  Maxpulse  Calories
0         60    110       130     409.1
1         60    117       145     479.0
2         60    103       135     340.0
3         45    109       175     282.4
4         45    117       148     406.0
5         60    102       127     300.0
6         60    110       136     374.0
7         45    104       134     253.3
8         30    109       133     195.1
9         60     98       124     269.0
10        60    103       147     329.3
11        60    100       120     250.7
12        60    106       128     345.3
13        60    104       132     379.3
14        60     98       123     275.0
15        60     98       120     215.2
16        60    100       120     300.0
17        45     90       112       NaN
18        60    103       123     323.0
19        45     97       125     243.0
--- Estatísticas simples -----------------
Media de Pulse: 103.9
Soma de Pulse: 2078
Max de Pulse: 117
Min de Pulse: 90
Contagem de Pulse: 20
mediana de Pulse: 103.0
Desvio padrão de Pulse: 6.711341539748807
Variação de Pulse: 45.04210526315789
```



```python
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>



# 9. 3D

## 9.1 Matplotlib


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

<br>
Fonte do exemplo acima: https://matplotlib.org/stable/gallery/mplot3d/projections.html<br>
<br>

[Voltar ao sumário](#sumário)<br>


## 9.2. Outro exemplo com Matplotlib

Outro exemplo com matplotlib: https://matplotlib.org/stable/gallery/mplot3d/box3d.html

![https://matplotlib.org/stable/_images/sphx_glr_box3d_001.png](https://matplotlib.org/stable/_images/sphx_glr_box3d_001.png)

Mais um exemplo: https://stackoverflow.com/questions/70911608/plot-3d-cube-and-draw-line-on-3d-in-python

![https://i.stack.imgur.com/YKoJ2.png](https://i.stack.imgur.com/YKoJ2.png)

[Voltar ao sumário](#sumário)<br>


## 9.3. Axes3D

```python
# importa as bibliotecas
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D 
import numpy as np

# Cria os eixos
axes = [5, 5, 5]

# Cria os dados
data = np.ones(axes)

# Controle transparencia
alpha = 0.9

# Controle cores
colors = np.empty(axes + [4])

colors[0] = [1, 0, 0, alpha] # vermelho
colors[1] = [0, 1, 0, alpha] # verde
colors[2] = [0, 0, 1, alpha] # azul
colors[3] = [1, 1, 0, alpha] # amarelo
colors[4] = [1, 1, 1, alpha] # cinza

# Plota a figura
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Voxels são usados para customizar tamanho, posição e cores
ax.voxels(data, facecolors=colors, edgecolors='grey')
```

<br>
Fonte do exemplo acima: https://www.geeksforgeeks.org/how-to-draw-3d-cube-using-matplotlib-in-python/ <br>
<br>

```
Em desenvolvimento
```

[Voltar ao sumário](#sumário)<br>





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
Autor: Prof. Dr. Monteiro.
Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) 
https://creativecommons.org/licenses/by-nc-sa/4.0/
```

## Observação
```
Primeira postagem em: Junho/2023.
```


## Estatísticas

### Estatísticas do Repositório

![GitHub stars](https://img.shields.io/github/stars/monteiro74/tutorial_python?style=social)
![GitHub forks](https://img.shields.io/github/forks/monteiro74/tutorial_python?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/monteiro74/tutorial_python?style=social)

![GitHub repo size](https://img.shields.io/github/repo-size/monteiro74/tutorial_python?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/monteiro74/tutorial_python?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/monteiro74/tutorial_python?style=flat-square)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/monteiro74/tutorial_python?style=flat-square)

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=monteiro74.tutorial_python)
![GitHub contributors](https://img.shields.io/github/contributors/monteiro74/tutorial_python?style=flat-square)

### Histórico de Atualizações

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=monteiro74&theme=github-compact)](https://github.com/monteiro74/tutorial_python)

### Estatísticas do Autor

[![GitHub Streak](https://streak-stats.demolab.com/?user=monteiro74&theme=default)](https://git.io/streak-stats)

![Stats](https://github-readme-stats.vercel.app/api?username=monteiro74&show_icons=true&theme=default&include_all_commits=true&count_private=true)

### Linguagens Mais Utilizadas

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=monteiro74&layout=compact&theme=default)](https://github.com/monteiro74/github-readme-stats)

### Links Úteis de Análise

- **Pulse:** [Visualizar atividade do repositório](https://github.com/monteiro74/tutorial_python/pulse)
- **Histórico de frequência de código:** [Ver gráfico](https://github.com/monteiro74/tutorial_python/graphs/code-frequency)
- **Atividade de commits:** [Ver detalhes](https://github.com/monteiro74/tutorial_python/graphs/commit-activity)
- **Tráfego:** [Ver estatísticas de visitantes](https://github.com/monteiro74/tutorial_python/graphs/traffic)

[Voltar ao sumário](#sumário)<br>


---
# Como Contribuir

Contribuições são bem-vindas! Se você deseja sugerir melhorias, reportar erros ou contribuir com novos exemplos, entre em contato:

- **Website:** [www.pontodeensino.com](https://www.pontodeensino.com)
- **Contato:** Prof. Dr. Emiliano Soares Monteiro

Você também pode abrir uma issue ou pull request neste repositório para sugerir alterações ou correções.

[Voltar ao sumário](#sumário)<br>


---
# Créditos

**Autor:** Prof. Dr. Emiliano Soares Monteiro

Este material foi desenvolvido e é mantido pelo Prof. Dr. Emiliano Soares Monteiro, com o objetivo de fornecer um recurso educacional de qualidade para estudantes e profissionais interessados em aprender Python.

- **Website:** [www.pontodeensino.com](https://www.pontodeensino.com)
- **GitHub:** [@monteiro74](https://github.com/monteiro74)

[Voltar ao sumário](#sumário)<br>


---
# Como Citar Este Material

Se você utilizar este material em trabalhos acadêmicos, projetos ou publicações, por favor cite adequadamente:

## Formato ABNT

```
MONTEIRO, Emiliano Soares. Tutorial sobre Python. 2023. Disponível em: https://github.com/monteiro74/tutorial_python. Acesso em: [data de acesso].
```

## Formato BibTeX

```bibtex
@misc{monteiro2023python,
  author       = {Monteiro, Emiliano Soares},
  title        = {Tutorial sobre Python},
  year         = {2023},
  publisher    = {GitHub},
  journal      = {GitHub repository},
  howpublished = {\url{https://github.com/monteiro74/tutorial_python}},
  note         = {Acesso em: [data de acesso]}
}
```

## Citação em Texto

Para citações no texto, utilize:

- **Formato autor-data:** (MONTEIRO, 2023)
- **Formato narrativo:** Monteiro (2023) apresenta exemplos práticos de Python...
- **Citação direta:** Conforme Monteiro (2023, p. 1), "Pequenos exemplos para uso da linguagem python..."

[Voltar ao sumário](#sumário)<br>

