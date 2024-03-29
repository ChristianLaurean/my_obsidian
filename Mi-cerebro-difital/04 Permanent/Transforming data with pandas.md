---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
---
# Trasformación de datos
Es una de las partes mas importantes del proceso y del éxito de una solución con datos. 

Si los datos se seleccionan en formato incorrecto o se pierde información durante la trasformación es muy posible que esos datos no generen valor.

 Usamos pandas para esto: 
 - Podemos [[¿Como Filtrar un DataFrames?]]
 - Crear Columnas
 - Cambiar tipos de datos
[[¿Como filtrar un DataFrame con Loc y ILoc?]] se usa para filtrar filas y columnas
Manipular fechas con pandas
- `to_datetime()`
- Convertirnos la columna a date time
```python
df["times"] = pd.to_datetime(df["times"], format="%Y%m%d%H%M%S")
# o
df["times"] = pd.to_datetime(df["times"], unit="ms")
```
# validar la trasformación

- Nos ayuda a mitigar riesgos
- Dabemos usar `head()`
 ```python
 df.nsmallest(10,["colum_date"])# valores mas pequeños
 df.nlargest(10,["colum_date"])# valores mas grandes
 ```
 