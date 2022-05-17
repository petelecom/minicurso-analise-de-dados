- [A biblioteca matplotlib](#a-biblioteca-matplotlib)
- [Grafico simples]()
- [Estilizando graficos]()
- [Diferentes tipos de Gráficos]()
- [Salvar graficos]()
- [Referências](#referencias)

----

### A biblioteca Matplotlib

Essa biblioteca fornece funções para gerar diversos tipos de gráficos e assim visualizar informações gráficamente.

- Para usar a ferramenta, devemos primeiro, instala-la:

```python
    pip install -U matplotlib
```
<br>

Conheça melhor a biblioteca:
<a href="https://matplotlib.org/"> Site oficial do projeto</a>

### Gráfico Simples
Como dito anteriormente utilizaremos a biblioteca Matplotlib. Para criar os gráficos utilizaremos o modulo PyPlot, para utiliza-lo é necessário fazer a importação:
```python
    import matplotlib.pyplot as plt
```
Uma vez importado o pyplot como "plt", é possível criar um gráfico de forma simples como mostrado no exemplo abaixo:
```python
In[]:
    # Criando um gráfico
    plt.plot(
        [1, 2, 3], 
        [1, 3, 6]
    )
    plt.show()
```
```python
Out[]:
```
<p align ="center"><img align=center src="plot.png"></p>

Assim, criamos um gráfico simples utilizando a biblioteca matplotlib.

### Estilizando gráficos 
Aqui, veremos mais parâmetros para criar um gráficos com mais informações e mais completo.
* Com auxilio dos argumentos de palavra-chave, será possível mudar: a espessura da linha (linewidth), a estilo da linha (linestyle), marcação no ponto (marker), legenda (label)
* Para atribuir titulo ao grafico e aos eixos serão utlizadas as funções 'title' e 'xlabel/ylabel', respectivamente.

Abaixo temos um exemplo:

```python
In[]:

    # Definindo variáveis
    x = [1, 2, 3]
    y = [1, 3, 6]

    # Criando um gráfico e atribuindo etiquetas
    plt.plot(x, y, linewidth=2, linestyle='--', marker='o', label = 'Uma legenda')
    plt.plot(y, x, linewidth=2, linestyle=':', marker='D', label = 'Outra legenda')

    # Atribuindo um título ao gráfico
    plt.title('Exemplo utilizando Plot')
    plt.xlabel('Variavel 1')
    plt.ylabel('Variavel 2')

    # Aplicando legenda
    plt.legend()

    # Exibindo o gráfico gerado
    plt.show()
```

```python
Out[]:
```
<p align ="center"><img align=center src="splot_aprimorado.png"></p>

