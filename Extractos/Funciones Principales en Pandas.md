---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
Hay ciertas **_funciones_** que son muy importantes y que siempre estaremos usando a la hora de hacer análisis de datos, para mayor facilidad y comprensión del DataFrame.

- **_Mostrar_** las primeras dos líneas de registro

```python
df_books.head(2) 
---> #muestra los primeros dos registros del dataFrame 
```

- Mostrar **los diferentes datos** que contiene el DataFrame

```python
df_books.info()
---> py
RangeIndex: 550 entries, 0 to 549        #numero de registro
Data columns (total 7 columns):          #total de columnas

 #   Column       Non-Null Count  Dtype  #tipos de cada columna
---  ------       --------------  -----  
 0   Name         550 non-null    object 
 1   Author       550 non-null    object 
 2   User Rating  550 non-null    float64
 3   Reviews      550 non-null    int64  
 4   Price        550 non-null    int64  
 5   Year         550 non-null    int64  
 6   Genre        550 non-null    object 
dtypes: float64(1), int64(3), object(3)
```

- Obtener diferentes **datos estadísticos** de las columnas numéricas.

```python
df_books.describe()
--->  User.Rating  Reviews   Price     Year
count    550       550       550       550
mean    4.618   11953.281    13.1      2014
std     0.226   11731.132    10.84     3.165
min      3.3        37         0       2009
25%      4.5      4058         7       2011
50%      4.7      8580        11       2014
75%      4.8    17253.25      16       2017
max      4.9      87841      105       2019 
```

- Mostrar los **últimos 5 registros** del DataFrame

```python
df_books.tail()
---> #muestra los ultimos 5 registros
```

- Obtener el **uso de la memoria** de cada columna

```python
df_books.memory_usage(deep=True)
--->
Index            128
Name           59737
Author         39078
User Rating     4400
Reviews         4400
Price           4400
Year            4400
Genre          36440
dtype: int64
```

- Obtener **_cuantos datos_** tenemos de algo en específico

```python
df_books['Author'].value_counts()
---> Muestra cuantos datos hay de cada autor
```

- **_Eliminar_** registros duplicados

```python
df_books.drop_duplicates()
```

- Ordenar los **_registros según valores_** de la columna (orden ascendente)

```python
df_books.sort_values('Year')
---> #ordena los valores de menor a mayor segun el año
```

- Ordenar los registros según valores de la columna **_(orden descendente)_**

```python
df_books.sort_values('Year', ascending=False)
---> #ordena los valores de mayor a menor segun el año
```