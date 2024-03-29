---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
cssclasses:
  - center-images
  - center-titles
  - page-manila
  - pen-black
---
Las tablas dinámicas son otra forma de calcular estadísticas resumidas agrupadas. 

## diferencia entre group by y tablas dinámicas

![[Pasted image 20240322164510.png]]

# agregando estadisticas

```python
import numpy as np
df_walmart.pivot_table(values="weekly_sales", index="type", aggfunc=np.median)


#Multiples estadisticas
df_walmart.pivot_table(values="weekly_sales", index="type", aggfunc=[np.median,np.mean])


# diferentes columnas
df_walmart.pivot_table(values="weekly_sales", index="type", columns="department")


# si tenemos datos faltantes podemos usar `fill_value=`
df_walmart.pivot_table(values="weekly_sales", index="type", columns="department", fill_value=0)

df_walmart.pivot_table(values="weekly_sales", index="type", columns="department", fill_value=0, margins=True)
# esto hace que se cree una nueva fila y columna que contiene la media de todo asi como las tablas dinamicas de excel

```


