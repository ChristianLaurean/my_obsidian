---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
cssclasses:
  - center-images
  - center-titles
  - image-borders
  - page-manila
  - pen-black
---
# Seleccionar columnas 

```python
df_avocado["year"] # -> Es un pandas.Series de la columa.
```

---

#### Seleccionar varias columnas

```python
# Selecionar varias columnas solo necesitamos doble [[]]
df_avocado[["year", "avg_price"]] # -> Retorna un DataFrame de las dos columnas
```

>[!tip] Uso de los corchetes
>- Los corchetes exteriores se encargan de las filas
>- Los corchetes interiores crean una lista con las columnas  
>```python
>df = ["year", "avg_price"]
>df_avocado[df]
>```

---

# Filtrar DataFrames

```python
df_avocado["year"] > 2016 # -> Filtramos y nos retorna bool
```

#### DataFrame

```python
df_avocado[df_avocado["year"] > 2016] # -> retorna el DataFrame filtrado
```

## Filtrando con texto

```python
df_avocado[df_avocado["size"] == "small"]
```


## Filtrando Fechas

```python
df_avocado[ df_avocado["date"] > "2015-10-01"]
```

## Múltiples condiciones

```python
is_tamaño = df_avocado["size"] == "small"
is_2017 = df_avocado["year"] == 2017
df_avocado[is_tamaño & is_2017]
```

**Múltiples condiciones en una sola linea**

```python
df_avocado[(df_avocado["size"] == "small") & (df_avocado["year"] == 2017)]
```

## Filtrar variables categóricas

```python
# .isin que es un IN en SQL
is_smaill_large = df_avocado["size"].isin(["smail","large"])
df_avocado[is_smaill_large]
```
