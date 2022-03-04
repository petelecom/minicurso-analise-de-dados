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

- desenvolvimento web;
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


### Listas
### Dicionários
### Strings
## Funções
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
## Módulos
## Importando módulos
## pip
