---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
cssclasses:
  - center-images
  - center-titles
  - page-manila
  - pen-black
---
Los datos nulos **_son dolores de cabeza_** para este mundo de la ciencia de datos y se van a encontrar mucho en nuestros DataFrames

- **Identificar** valores nulos en un DataFrame
```python
df.isna()
```
---
![[Pasted image 20240323152141.png|300]]

---
**Sumamos los valores NaN** -> retorna cuantos valores NaN tiene cada columna.
![[Pasted image 20240323152250.png|300]]
 
 ---
**Podemos graficar los valores NaN**

![[Pasted image 20240323152411.png]]

---
**Borrar valores NaN**

- **Eliminar** valores nulos

```python
df.dropna()
--->  Col1   Col2   Col3
0       1      4      a
2       3      6      c
```

>[!danger] No es recomendable si hay muchos valores NaN
>- Lo mejor es usar otras técnicas


--- 
Opciones mas recomendables:
- Sustituir los valores nulos **por una cadena**

```python
df.fillna('Missing')
--->  Col1   Col2   Col3
0       1.0    4.0     a
1       2.0  Missing   b
2       3.0    6.0     c
3       Missing 7.0  Missing		
```

tambien le podemos pasar un dicionario

```python
df.fillna(value={"colum1":0, "colum2":0.5}, axis=1)
```

- Tambien podemos pasarle una columna al metodo fillna

```python
df["column"].fillna(["Columna_cambiar"], inplace=true)
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

---
- Sustituir valores nulos por valores de **interpolación**

```python
df.interpolate()
---->    Col1   Col2   Col3
0           1      4      a
1           2      5      b
2           3      6      c
3           3      7     None	  
```


---


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

