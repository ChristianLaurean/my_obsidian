---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
## .loc

Filtra según un **_label_**


```python
df_books.loc[:]
---> #muestra todos los datos del dataFrame
```

Mostrar un rango de filas tomando en cuenta el **_start y el end_**

```python
df_books.loc[0:4] 
---> #muestra los datos de la fila 0 a la fila 4
```

- Filtrando por **_filas y columnas_**

```python
df_books.loc[0:4, ['Name', 'Author']] 
----> #filtra los datos de la fila que va de 0 a 4 y de las columnas Name y Author
```

- Podemos modificar los valores de una **_columna específica_** del dataFrame

```python
df_books.loc[:, ['Reviews']] * -1
---> #multiplica por -1 todos los valores de la columna Reviews
```

- Filtrar datos que cumplan una **_condición_** determinada

```python
df_books.loc[:, ['Author']] == 'JJ Smith' 
----> #muestra la columna Author con True en los valores que cumplen la condicion y False para los que no la cumplen
```

## .iloc

Filtra mediante **_índices_**.

```python
df_books.iloc[:] ---> #muestra todos los datos del dataframe
```

- Filtrar datos según los índices de las **_filas y las columnas_**

```python
df_books.iloc[:4, 0:2] ---> #muestra los datos de las filas que van de 0 a 3 y las columnas con indices 0 y 1
```

- Buscar un **_dato específico._**

```python
df_books.iloc[1,3] ---> #muestra el dato alojado en la fila 1 columna 3
```