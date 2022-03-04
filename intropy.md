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
<p style='text-align: justify;'>List é uma classe que agrupa dados, diferentemente do tuple as listas permitem modificações de seus elementos. Para criar uma lista </p>

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


### Dicionários
### Strings
## Funções
## Laços
## Classes
## Módulos
## Importando módulos
## pip
