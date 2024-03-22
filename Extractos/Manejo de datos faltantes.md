---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
Los datos nulos **_son dolores de cabeza_** para este mundo de la ciencia de datos y se van a encontrar mucho en nuestros DataFrames

- **Identificar** valores nulos en un DataFrame

```python
df.isnull()
---->    Col1   Col2   Col3
0       false   false  false
1       false   true   false
2       false   false  false
3       true    false  true
```

- Identificar valores nulos con un valor **numérico**

```python
df.isnull()*1
---> Col1   Col2   Col3
0       0      0       0
1       0      1       0
2       0      0       0
3       1      0       1
```

- Sustituir los valores nulos **por una cadena**

```python
df.fillna('Missing')
--->  Col1   Col2   Col3
0       1.0    4.0     a
1       2.0  Missing   b
2       3.0    6.0     c
3       Missing 7.0  Missing		
```

- Sustituir valores nulos por una **medida estadística** realizada con los valores de las columnas

```python
df.fillna(df.mean())
---->    Col1   Col2   Col3
0           1      4      a
1           2      5.667  b
2           3      6      c
3           2      7     None
```

- Sustituir valores nulos por valores de **interpolación**

```python
df.interpolate()
---->    Col1   Col2   Col3
0           1      4      a
1           2      5      b
2           3      6      c
3           3      7     None	  
```

- **Eliminar** valores nulos

```python
df.dropna()
--->  Col1   Col2   Col3
0       1      4      a
2       3      6      c
```