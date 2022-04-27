


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
