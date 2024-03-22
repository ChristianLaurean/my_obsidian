---
Author: Coderhouse
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
# ¿Qué es la librería Pandas?


Pandas es una librería de python que nos facilita la manipulación  de datos a través de un conjunto de métodos y estructuras.

- Es compatible con numpy

>[!warning] Todo esto ocurre en memoria
>Si cargamos un DataSet muy pesado a pandas esto estara en [[Ram|memoria]] y necesitaremos mucha memoria para poder procesarlos.

# Estructuras dundamentales

Series (1D)
![[Pasted image 20240221090422.png]]

DataFrames (2D)

![[Pasted image 20240221090448.png]]

>[!tip] Recuerda
>Una columna de un dataframe es un Series
>Un DataFrame tiene varias columnas y filas

Paneles (3D)
![[Pasted image 20240221090542.png]]

# Pandas DataFrames

- Son una exención del os objetos series(1D)
- Consta de Columnas y filas
- Cada fila contiene un [[Metodo index| indice]] asociado
![[Pasted image 20240221090848.png]]

# instalar pandas

`pip install pandas`
`import pandas as pd`

## Crear un DataFrame

```python
data = {"nombres": ["juan","Pedro","Marcos"], "Edad":[13,18,24]}
df = pd.DataFrame(data)
```

### Agregaciones

`df['Edad'].max()`