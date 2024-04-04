---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - center-images
  - center-titles
  - page-white
  - pen-black
---
# Trasformación de datos
Es una de las partes mas importantes del proceso y del éxito de una solución con datos. 

Si los datos se seleccionan en formato incorrecto o se pierde información durante la trasformación es muy posible que esos datos no generen valor.

---
# Consideraciones 

- Debo de saber que estructura van a tener mis datos en el target. 
- Tener en claro como voy a relacionar las distintas fuentes(Si no sabes como es importante hacer un [[Analisis exploratorio de los datos]])
- [[Normalización]] 
- [[¿Como Eliminar duplicados en pandas?|Manejar duplicados]]
- [[¿Como manejar datos faltantes en Pandas?]]
- [[¿Como usar Groupby con pandas?| ¿Debo agrupar los datos?]]

## Uso de pandas
 Usamos pandas para esto: 
 - Podemos [[¿Como Filtrar un DataFrames?]]
 - Crear Columnas [[¿Como crear y actualizar Columnas en un DataFrames?]]
 - Cambiar tipos de datos

[[¿Como filtrar un DataFrame con Loc y ILoc?]] se usa para filtrar filas y columnas
Manipular fechas con pandas


---


# Validar la trasformación

- Nos ayuda a mitigar riesgos
- Dabemos usar `head()`

 ```python
 df.nsmallest(10,["colum_date"])# valores mas pequeños
 df.nlargest(10,["colum_date"])# valores mas grandes
 ```
 