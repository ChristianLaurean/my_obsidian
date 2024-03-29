---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
# Estadisticas resumen

```python
df_avocado["avg_price"].mean() 
df_avocado["avg_price"].median() 
df_avocado["avg_price"].mode() 
df_avocado["avg_price"].min() 
df_avocado["avg_price"].max()
df_avocado["avg_price"].var()
df_avocado["avg_price"].std() 
df_avocado["avg_price"].sum() 
df_avocado["avg_price"].quantile() 
```

**Tambien se puede con fechas**

```python
df_avocado["date"].max()
```

# Metodo `agg` nos permite calcular estadisticas resumidas

```python
df_avocado["avg_price"].agg("max")
```

```python 
def p30(df):
    return df.quantile(0.3)

df_avocado["avg_price"].agg(p30)

# con lambda
df_avocado["avg_price"].agg(lambda p:p.quantile(0.3))
```


----
 ```python
 df_avocado[["avg_price", "year"]].agg(lambda p:p.quantile(0.3))

# Multiples agregaciones a la vez
df_avocado["avg_price"].agg([lambda p:p.quantile(0.3),"max"])
```

---
# Estadísticas acumulativas

```python
df_avocado["avg_price"].cummax()
df_avocado["avg_price"].cummin()
df_avocado["avg_price"].cumsum()
```

 
# Contar 

```python
df["type"].value_counts()

df["type"].value_counts(sort=True)

# sacamos proporciones dependiendo del total o porcentage
u["type"].value_counts(normalize=True)
```

