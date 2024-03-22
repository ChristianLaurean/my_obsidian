---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
Muchas ocasiones necesitamos agregar, eliminar o separar datos y pandas nos ofrece varias funciones para que este proceso se vuelva mucho más sencillo.


- Eliminar columnas de la salida pero no del DataFrame

```python
df_books.drop('Genre', axis=1).head()
df.drop(['Genre','Author'],axis=1)
---> #elimina la columna Genre de la salida pero no del dataFrame
```

- Eliminar una columna

```python
del df_books['Price'] 
---> #elimina la columna Price del dataFrame
```

- Eliminar filas

```python
df_books.drop(0, axis=0)
---> #elimina la fila 0 del dataFrame
```

- Eliminar un conjunto de filas mediante una lista

```python
df_books.drop([0,1,2], axis=0)
---> #elimina las filas 0, 1 y 2 del dataFrame
```

- Elimina un conjunto de filas mediante un rango

```python
df_books.drop(range(0,10), axis=0)
---> #elimina las primeras 10 filas del dataFrame
```

- Agregar una nueva columna con valores Nan

```python
df_books['Nueva_columna'] = np.nan
---> #Crea una nueva columna con el nombre de Nueva_columna de valores Nan
```

- Mostrar el número de filas o columnas que tiene un DataFrame

```python
df_books.shape[0]
---> #Muestra el numero de filas que posee el dataFrame
```

- Agregar valores a una nueva columna

```python
data = np.arange(0, df_books.shape[0])
```

- Crear una nueva columna y agregar los valores almacenados en el array

```python
df_books['Rango'] = data
---> #Crea una nueva columna llamada Rango con los valores del array 
```

- Para añadir filas se utiliza la función `append` de Python añadiendo como parámetro una lista, diccionario o añadiendo los valores manualmente.

```python
new = pd.concat([df_books, df_books.loc[:0]])
---> #Duplica las filas
```
