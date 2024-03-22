---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---


## Concat

- **Concatenar** los DataFrames

```python
pd.concat([df1,df2])# Es el sustituto del append
```

- **Corregir** los índices

```python
pd.concat([df1,df2], ignore_index= True)
---> A  B   C   D
0   A0  B0  C0  D0
1   A1  B1  C1  D1
2   A2  B2  C2  D2
3   A3  B3  C3  D3
4   A4  B4  C4  D4
5   A5  B5  C5  D5
6   A6  B6  C6  D6
7   A7  B7  C7  D7
```

- Por **axis 1**

```python
pd.concat([df1,df2], axis = 1)
---> A  B   C   D   A.1 B.1 C.1 D.1
0   A0  B0  C0  D0  A4  B4  C4  D4
1   A1  B1  C1  D1  A5  B5  C5  D5
2   A2  B2  C2  D2  A6  B6  C6  D6
3   A3  B3  C3  D3  A7  B7  C7  D7
```

## Merge


- **Unir** el DataFrame `Der` a `Izq`

- Hay diferencias entre algunas columnas, por esa razón hay que **separarlos** de esta manera:

```python
df_merge = df.merge(df_izq, how='left', left_on='columna_relaciona_con_la_otra', right_on='Column' )

df_merge = df.merge(df_izq, how='left', on='columna_relaciona_con_la_otra' )
```


- Si tenemos un `NaN`en nuestro DataFrame, pandas **no lo detectará como un mach**. Se soluciona con `How`, dando así, una preferencia.

```python
izq.merge(der, left_on = 'key', right_on='key_2', how='left')
---> key A  B   key_2   C   D
0   k0  A0  B0  k0    C0  D0
1   k1  A1  B1  k1    C1  D1
2   k2  A2  B2  k2    C2  D2
3   k3  A3  B3  NaN  NaN  NaN
```

# join 

`Join` Es otra herramienta para hacer exactamente lo mismo, una combinación. La diferencia es que **join va a ir a los índices y no a columnas específicas.**


- Combinamos `izq` con `der`

```python
izq.join(der)
---> A  B   C   D
k0  A0  B0  C0  D0
k1  A1  B1  nan nan
k2  A2  B2  C1  D1
```

- Traer todos los datos aunque no hagan match.

```python
izq.join(der, how = 'outer')
---> A  B   C   D
k0  A0  B0  C0  D0
k1  A1  B1  nan nan
k2  A2  B2  C1  D1
k3  nan nan C2  D2
```