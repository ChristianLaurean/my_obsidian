---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
---
La persistencia de los datos es una mejor practica que puede y debe ocurrir en múltiples etapas de una pipeline.

La persistencia en un archivo
Permite tomar una instantanea en varios puntos del proceso.
Es útil cuando se recupera de una falla y es esencial si es difícil volver a adquirir datos de un sistema fuente.

```python
df.to_csv("nombre_file.csv")
df.to_parquet("nombre_file.csv")
df.to_json("nombre_file.csv")
```

**Parámetros para ser guardados**

`header=True o lista para asignar una AS a los nombres de la columns`

`index=True`: EL index se escribirá en el archivo.
`sep=","` : nos sirve para saber como separar las columnas en un archivo csv

# validad si hay persistencia en los datos
usamos un programa para verificar si la ruta del archivo esta, si no esta entonces False.
