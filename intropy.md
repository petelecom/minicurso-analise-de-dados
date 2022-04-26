# Introdução ao python

- [História](#história)
- [Linguagem Interpretada](#linguagem-interpretada)
- [Palavras Reservadas](#)
- [Estrutura de dados](#estrutura-de-dados)
  - [Utilizando variáveis](#variáveis)
  - [Tuples](#tuples)
  - [Listas](#listas)
  - [Dicionários](#dicionários)
  - [Strings](#strings)
- [Funções](#funções)
- [Laços](#laços)
- [Classes](#classes)
- [Módulos](#módulos)
- [Importando módulos](#importando-módulos)
- [pip](#pip)


## História

Python é uma linguagem de programação de alto nível, interpretada de script, imperativa, orientada a objetos, funcional, de tipagem dinâmica e forte. Foi lançada por Guido van Rossum em 1991 e posteriormente desenvolvido pela Python Software Foundation.

#### Utilidades:

- desenvolvimento web (lado do servidor);
- desenvolvimento de software;
- matemática;
- analise de dados;
- inteligencia artificial (I.A).

#### Informações: 

- A versão principal mais recente do Python é o Python 3, que usaremos neste minicurso. 
- É possível escrever Python utilizando uma IDE (ambiente de desenvolvimento integrado), Pycharm, Netbeans, Sublime, Eclipse, Visual studio code, entre outros.


## Linguagem Interpretada

<a name = "estrutura-de-dados"/>

### Variáveis
### Tuples
[Documentação](https://docs.python.org/3/library/stdtypes.html?highlight=tuples#tuple)
<p style='text-align: justify;'>Tuple é uma classe que agrupa dados. Uma vez criado o tuple não pode: remover, mudar a ordem ou adicionar novos elementos.
Usado para quando determidado dado tem uso de apenas leitura, garantindo segurança da aplicação.</p>

```python
vetor = (1, 4, -2)
oneItem = (1,)
```
<p style='text-align: justify;'> Quando deseja-se criar um tuple de apenas um único elemento deve conter a virgula. </p>

<p style='text-align: justify;'> Os itens são acessados pelo índice, o primeiro elemento é o índice 0. Caso ocorra o acesso de um índice inválido, é lançado um erro.
 A sintaxe é:</p>

```python
variavel[indice]
```

```python
vetor[0] # acessa o primeiro elemento do tuple, o valor obtido é 1
oneItem[1] # É obtido um erro com a mensagem "IndexError: tuple index out of range"
```
<p style='text-align: justify;'> Também é possível acessar com índices negativos, -1 para o último elemento, -2 para o penúltimo e assim por diante. </p>

### Listas

[Documentação](https://docs.python.org/3/library/stdtypes.html?highlight=list#list)
<p style='text-align: justify;'>List é uma classe que agrupa dados, diferentemente do tuple as listas permitem modificações de seus elementos. Para criar uma lista: </p>

```python
vetor = [1, 4, -2]
oneItem = [1]
```
<p style='text-align: justify;'> Os itens são acessados pelo índice, o primeiro elemento é o índice 0. Caso ocorra o acesso de um índice inválido, é lançado um erro.
 A sintaxe é:</p>

```python
variavel[indice]
```

```python
vetor[0] # acessa o primeiro elemento do tuple, o valor obtido é 1
oneItem[1] # É obtido um erro com a mensagem "IndexError: list index out of range"
```
<p style='text-align: justify;'> Também é possível acessar com índices negativos, -1 para o último elemento, -2 para o penúltimo e assim por diante. </p>


### Dicionários

[Documentação](https://docs.python.org/2/tutorial/datastructures.html#dictionaries)

Os dicionários em python associa um objeto a uma chave. A chave do dicionário deve ser um objeto "hashable", ou seja, um objeto imutável como números, tuples e strings. O objeto associado a chave pode ser qualquer objeto sem restrições. Os objetos que cada chave associa podem ser alterados.

<p></p>

- Para criar um dicionário utiliza-se as seguintes sintaxes

```Python
  variavel1 = {} # dicionario vazio
  variavel2 = dict() # dicionario vazio
  variavel3 = dict(Terra=4.545e9, Marte = 4.605e9)
  variavel4 = {'Terra':4.545e9, 'Marte': 4.605e9 , 1:2, 1.5:6, 1+2j:10, (1,1):0.5, 'dict1':variavel1}
```
 - Como mencionado antes os dicionários são mutáveis, então é possivel adicionar novas chaves a eles
 
```Python
  variavel1['Terra']  = variavel4['Terra']
  variavel2['Terra'] = 4.543e9
```
- E também remover uma chave do dicionário

```Python
  del variavel4['Terra']
  del variavel3['Marte']
```
- Para verificar se uma chave existe no dicionário pode-se utilizar a palavra reservada "in"

```Python 
  if 'Terra' in variavel4:
    print("'Terra' é uma chave no dicionario 'variavel4'")
  else:
    print("'Terra' não é uma chave no dicionario 'variavel4'")
```


### Strings
  
  [Documentação](https://docs.python.org/3/library/stdtypes.html#text-sequence-type-str)
  
  As strings são cadeias de caracteres que representam textos. Em python uma vez criada a string não pode ser moficada, isto é, não pode-se alterar nenhum caractere da mesma, para alterar uma string cria-se uma nova string modificada. As strigs em python são criadas utilizando aspas duplas ou simples, quando utiliza-se uma sequencia de 3 aspas indica que a string é multilinha. As classes possuem um metodo que retorna uma representação de si no formato de string, util para mostrar na tela os seus valores, e o python3 simplifica o acesso a esse metodo, para isso antes de declarar a string adiciona-se a letra f.
  
- Sintaxe para criar uma string
  
```Python

str1 = 'texto1'
str2 = "texto2"
str3 = """ String multilinha
essa é a segunda linha """
nome  = "Pet Telecom"
str4 = f"Bem vindo {nome}" # string criada  'Bem vindo Pet Telecom'
```

## Funções

Quando temos um trecho de script que será utilizado diversas vezes não eficaz e nem otmizado ficar repetindo as mesmas linhas toda vez que for necessário, para resolver isso o python permite criar suas próprias funções. As funções são como pequenos scripts que tem uma finalidade, elas possuem parametros de entrada e pode devolver objetos para quem a chamou. 

Por exemplo, você se encontra em um problema que será feito a media de variáveis (ignorando as função mean já disponível no Python)


```Python
  x = [1, 2, 54, 10, 14, 4]
  y = [4, 6, 7, -5, 13, 50]
  
  media_x = 0
  for xi in x:
    media_x +=  xi
  media_y = 0
  for yi in y:
    media_y +=  yi
```

Note que quanto mais vezes for necessário utilizar a média mais linhas repetidas serão adicionadas, a função tem a seguinte sintaxe:

```Python
def  name_function(param1,param2, *args, **kwargs):
    # corpo
    return var1, var2, var3
```
Dentro dos parenteses coloca-se os parametros de entrada da função, o parametro "*args" é utilizado para adicionar vários parametros e o "** kwaegs" é um dicionário. A função media fica:
```Python
def media(lista):
  u = 0
  for vi in lista:
    u += vi
  return u
```

Assim o script fica mais enxuto facilitando a leitura e correção de possíveis bugs

```Python
  x = [1, 2, 54, 10, 14, 4]
  y = [4, 6, 7, -5, 13, 50]
  
  media_x = media(x)
  media_y = media(y)
```


 
## Laços

### Condição com o IF/ELSE

- Vamos ver no codigo como funcionaria uma estrutura de if/else. Digamos que, uma pessoa abaixo dos 18 anos seja adolescente senão, será considerada adulta. Coloquemos isso em codigo:
```python
    if idade < 18:
        print('Você é adolescente!')
    else:
        print('Você é adulto!')

Na linguagem Python, a indentação é utilizada para demarcar os blocos de código, e são obrigatórios quando se usa estruturas de controle.
```

- Também é possível checar mais de uma condição com o __elif__. É a abreviatura para else __if__. Ou seja, se o __if__ for falso, testa outra condição antes do __else__:

```python
    idade = 18
    if idade < 18:
        print('Você é Adolescente!')
    elif idade > 50:
        print('Você é Velho!')
    else:
        print('Você é Adulto!')
```

- Note que quando uma condição for verdadeira, aquele bloco de código é executado e as demais condições (__elif__ e __else__) são puladas:

```python
In[]:

    a = 1
    if a == 1:
        print("é 1")
    elif a >= 1:
        print("é maior ou igual a 1")
    else:
        print("é qualquer outra coisa")
        
```

```python
Out[]:

    é 1
```

## Classes

A linguagem python é orientada a objetos, uma classe serve para criar um modelo de um objeto e de quais atríbutos e metódos aquele objeto quando instânciado terá. Uma instância é o objeto já criado.  A sintaxe para criar uma classe é:

```Python
 class NomeClass(ClasseMae): # a classe Mãe quando não inserida é implicito que a classe mãe é a Object
  def __init__(self, arg1):
     self.atr1 = arg1
  def method1(self,arg1):
    pass
```
Todos os metodos são análogos a uma função, com a diferença que o primeiro argumento (normalmente com o nome self) é a instância da classe.

## Módulos

Os módulos servem para agrupar todas as classes, funções e valores  para um API. Para criar seu próprio módulo basta criar um arquivo com extensão .py com as funções e classes, e em outro arquivo importar o módulo.

## Importando módulos

Para importar um módulo utiliza-se a seguinte sintaxe:

```Python
import nome_modulo

nome_modulo.class1()
nome_modulo.class2()
nome_modulo.func1(1, 2)
```
Também é possível importar apenas uma classe ou função do modulo

```Python
from nome_modulo  import class1, func1

class1()
func1(1, 2)
```
Caso tenha algum problema com funções com o mesmo nome ou classe pode ser utilizado o comando "as"


```Python
from nome_modulo import func1 as func2
import numpy as np
import pandas as pd

```


## pip


O pip é uma ferramenta de gerenciamento de bibliotecas e APIs do python, com ele é facil adicionar uma nova biblioteca, na linha de comandos ele pode ser usado para instalar a API numpy que possui classes e funções para manipulação de matrizes e vetores.


```cmd
pip install numpy
```
