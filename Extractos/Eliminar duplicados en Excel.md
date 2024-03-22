---
Author: DataCAMP
Category: Limpieza de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
- Eliminamos las filas que se encuentren repetidas dentro de una columna.
- Hace que tengamos datos únicos
```python
df_walmart.drop_duplicates(subset="department")

df_walmart.drop_duplicates(subset=["department","type"])
```