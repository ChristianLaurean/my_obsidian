---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - center-titles
  - center-images
  - page-white
---


# **Persistencia de los datos**


Capturar múltiples instantáneas de los datos a medida que atraviesan el pipeline es esencial para garantizar su integridad y trazabilidad. Esto implica almacenar los datos de manera adecuada en archivos u otros medios de almacenamiento, lo que facilita la recuperación en caso de fallos y permite reiniciar el proceso desde el punto exacto de la interrupción.

![[Pasted image 20240326091441.png]]

- Los archivos verdes muestran lugares lógicos para conservar datos dentro de la pipeline
 - El pipeline puede volverse a ejecutar desde el ultimo punto de la falla y en lugar de empezar al inicio
- La persistencia de los datos facilita la documentación de las operaciones realizadas

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
