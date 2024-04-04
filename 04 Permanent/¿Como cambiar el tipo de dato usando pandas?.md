---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
cssclasses:
  - page-white
  - center-images
  - center-titles
---


# Tipo de dato fecha

- `to_datetime()`
- Convertirnos la columna a date time

```python
df["times"] = pd.to_datetime(df["times"], format="%Y%m%d%H%M%S")
# o
df["times"] = pd.to_datetime(df["times"], unit="ms")
```

# Otros tipos de datos
`astype("int")`

```python
df.astype("int32")
```
