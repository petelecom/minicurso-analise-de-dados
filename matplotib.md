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
        [1, 2, 3]
    )
    plt.show()
```
```python
Out[]:
```
<p align ="center"><img align=center src="plot.png"></p>

