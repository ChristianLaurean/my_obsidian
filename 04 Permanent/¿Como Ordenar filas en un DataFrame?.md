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
# Order de las filas

**Forma normal**
`df_avocado.sort_values("avg_price",ascending=False)`

---
### Ordenando múltiples columnas 

```python
# Podemos ordenar multiples columnas pasandole una lista
# Tambien podemos pasarle una lista para ver la forma que quieres que se ordenen los datos.
df_avocado.sort_values(["avg_price", "nb_sold"], ascending=[False, True])
```
