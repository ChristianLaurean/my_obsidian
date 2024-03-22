---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
**Creamos una nueva columna del DataFrame usando otra columna con el mismo tamaño del DataFrame.**

```python
df_avocado["nombre_nueva_columns"] = df_avocado["avg_price"] + 10
```

**Sumamos dos dataframes para crear una nueva columna**

```python
df_avocado["total"] = df_avocado["avg_price"] + df_avocado["nb_sold"]
```
