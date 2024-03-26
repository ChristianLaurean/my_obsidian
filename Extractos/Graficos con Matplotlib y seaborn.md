---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
# instalación y importación
# diseñada para numpy

```python
pip install matplotlib

import matplotlib.pyplot as plt
import numpy as np
```


## Estilos

```python
print(plt.style.available)
plt.style.use('seaborn-v0_8-whitegrid')
```
# grafico de lineas

```python
# Pandas
pais = df[df['country'] == 'Mexico']
#matplotlib
plt.plot(x,y,label='Mexico', color='g')
plt.title('Crecimiento de la población a lo largo del tiempo')
plt.xlabel('Año')
plt.ylabel('Población')
plt.legend()
plt.grid(True)
plt.show()
```


# barras

```python
df.plot(kind="bar",tutle="" )

O
plt.bar(x,y,width=0.5,color=['blue','yellow','red','green'])
plt.xticks()
plt.show()
#horizontal
plt.barh(x,y,width=0.5,color=['blue','yellow','red','green'])
plt.xticks()
plt.show()
```

# histograma

```python
df["colum"].hist(bins=2)
plt.show()
```

# grafica de pie

```python
plt.pie(y)
plt.show()
```

# boxplot

```python
plt.boxplot(y)
plt.show()
```

# Seaborn

Diseñada para [[Pandas]]


```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt


sns.set_theme(style="dark",palette="muted")


sns.barplot(x='country',y='population',data=data)
plt.show()
```

## Parametros mas usados en sns


```python
sns.displot(x='population',data=paises, hue='country',kind='kde',palette='dark')
plt.show()
```

# variables categoricos

```python
sns.countplot(data=paises, x='year', hue='country')
plt.show()
```