

- [A biblioteca pandas](#a-biblioteca-pandas)
- [Primeiro Script](#primeiro-scrip-usando-pandas)
- [Pandas Series](#pandas-series)
- [Pandas DataFrames](#pandas-dataframes)
- [Lendo Arquivos CSV](#lendo-arquivos-csv)
- [Lendo Arquivos JSON](#lendo-arquivos-json)
----

### A biblioteca pandas

Essa api é útil para trabalhar com conjuntos de dados, ela fornece funções para manipular, analisar e explorar dados.
Com essa api as informações podem ser extraídas dos conjuntos de dados, os dados relevantes são muito importantes na ciência de dados.
    
<p align="center"> Ciência de dados: É um ramo da ciência da computação onde estudamos como armazenar, usar e analisar dados para derivar informações deles.</p>

### Instalação da biblioteca

O pandas pode ser facilmente instalado utilizando a linha de comando:

```cmd
pip install pandas
```

Para verificar informações da biblioteca utiliza-se a linha de comandos:

```cmd
pip show pandas
```

----

### Primeiro scrip usando pandas

```python
import pandas
meusDados = {
  'carros': ["Camaro", "HB20", "Gol"],
  'portas': [2, 4, 2]
}
mvar = pandas.DataFrame(meusDados)
print(mvar)
```

Saída:
```
   carros  portas
0  Camaro       2
1    HB20       4
2     Gol       2
```

Normalmente a biblioteca é importada com "pd"

```Python
import pandas as pd
```

Assim o script acima fica:
```python
import pandas as pd
meusDados = {
  'carros': ["Camaro", "HB20", "Gol"],
  'portas': [2, 4, 2]
}
mvar = pd.DataFrame(meusDados)
print(mvar)
```

----

### Pandas Series

Uma Série pandas é como apenas uma única coluna em uma tabela, um array unidimensional com valores de qualquer tipo:

```Python
import pandas as pd
dados = [1, 3, 5, -1, 8]
serie = pd.Series(dados)
print(serie)
```
Saída:
```
0    1
1    3
2    5
3   -1
4    8
dtype: int64
```

Se não for especificado, cada valor será etiquetado com o seu índice partindo do 0. Essa etiqueta serve para acessar os dados como o exemplo abaixo:
```Python
print(serie[0])
```
Saída:
```
1
```

Para adicionar etiquetas utiliza-se o parâmetro "index" no construtor da serie:


```Python
import pandas as pd
dados = [1, 3, 5, -1, 8]
serie = pd.Series(dados, index = ["a", "b", "c", "d", "e"])
print(serie)
```
Saída:
```
a    1
b    3
c    5
d   -1
e    8
dtype: int64
```

Também pode-se utilizar um dicionário para criar uma serie, assim a chave será entendida como etiqueta:

```Python
import pandas as pd
dados = {"Camaro":2014, "Fusca": 1984, "Opala":1991}
serie = pd.Series(dados)
print(serie)
```
Saída:
```
Camaro    2014
Fusca     1984
Opala     1991
dtype: int64
```

O uso do index agora é utilizado para selecionar quais itens do dicionário serão adicionados:
```Python
import pandas as pd
dados = {"Camaro":2014, "Fusca": 1984, "Opala":1991}
serie = pd.Series(dados, index = ["Opala", "Camaro"])
print(serie)
```
Saída:
```
Opala     1991
Camaro    2014
dtype: int64
```

----

### Pandas DataFrames

Os conjuntos de dados geralmente são tabelas multidimensionais, chamados de "DataFrames". 
Séries são como colunas, DataFrames são como tabelas possuindo linhas e colunas.

Para criar um dataFrame:
```Python
import pandas as pd
data = {
  "caloria": [420, 380, 390],
  "duracao": [50, 40, 45]
}
df = pd.DataFrame(data)
print(df) 
```
Saída:
```
   caloria  duracao
0      420       50
1      380       40
2      390       45
```

Para acessar os valores da tabela o dataFrame fornece o atributo loc (acessa as linhas), quando passado um único valor o retorno é uma serie e quando passado uma lista o retorno é um dataFrame:

Para criar um dataFrame:
```Python
import pandas as pd
data = {
  "caloria": [420, 380, 390],
  "duracao": [50, 40, 45]
}
df = pd.DataFrame(data)
print(df.loc[0]) 
print("-"*40)
print(df.loc[[0,1]]) 
```
Saída:
```
caloria    420
duracao     50
Name: 0, dtype: int64
----------------------------------------
   caloria  duracao
0      420       50
1      380       40
```

Assim como as séries os dataFrames podem ter etiquetas:

```Python
import pandas as pd
data = {
  "caloria": [420, 380, 390],
  "duracao": [50, 40, 45]
}
df = pd.DataFrame(data, index=["dia1", "dia2", "dia3"])
print(df) 
```
Saída:
```
      caloria  duracao
dia1      420       50
dia2      380       40
dia3      390       45
```


----

### Lendo Arquivos CSV

Se você tiver um conjunto de dados armazenado em um arquivo csv, o pandas consegue ler e coloca-los em um dataframe.

```Python
import pandas as pd
df = pd.read_csv('dados.csv')
print(df)
```

Arquivos CSV (comma separated files - arquivos separados por virgula) são comumente usados para armazenar grandes conjuntos de dados, utilizam o modo texto para armazenamento facilitando a leitura e escrita dos mesmos. Para os exemplos será utilizado o arquivo "dados.csv" que pode ser obtido <a href="https://raw.githubusercontent.com/petelecom/minicurso-analise-de-dados/main/dados.csv"> aqui</a>. 

Para mostrar a tabela inteira pode-se utilizar o metodo "to_string":

```Python
import pandas as pd
df = pd.read_csv('dados.csv')
print(df.to_string())
```

----

### Lendo Arquivos JSON

Pandas também consegue importar dados de um arquivo json, o arquivo utilizado será "dados.json" que pode ser obtido <a href="https://raw.githubusercontent.com/petelecom/minicurso-analise-de-dados/main/dados.json"> aqui</a>.

O script abaixo importa os dados de um arquivo json:
```
import pandas as pd 
df = pd.read_json('dados.json')
print(df.to_string())
```

