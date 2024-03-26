---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
**INDEX**

`set_index("column")` nos ayuda a mover una columna al indice
- `df_walmart.set_index("type")`
---
`.reset_index()` **Nos sirve para desahacer el index que le habiamos puesto.**
`.reset_index(drop=True)` **Nos sirve para quitar el indice y eliminarlo..**
- `df_walmart.reset_index(drop=True)`

```python
# podemos agregarle varias columnas al indice
test = df_walmart.set_index(["type"],["is_holiday"])
```

`.sort_index()` nos sirve para ordenar los indices.

`df_walmart.sort_index(level="column",ascending=False)`

# ejemplo interesante
```python
# Fija el índice de temperatures por country y city
temperatures_ind = temperatures.set_index(["country","city"])

# Lista de tuplas, Brazil, Rio De Janeiro y Pakistan, Lahore
rows_to_keep = [("Brazil","Rio De Janeiro"), ("Pakistan","Lahore")]

# Subdivide con rows to keep
print(temperatures_ind.loc[rows_to_keep])
```