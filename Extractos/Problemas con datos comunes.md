---
Author: DataCAMP
Category: Transformación_datos
Type: Apunte
Status: Terminado
relación: "[[Transformación de datos]]"
---
# Tipos de datos
Es importante que nuestros datos tengan el tipo de dato adecuado.

`.dtypes` Nos ayuda a ver el tipo de datos de cada columna.
`.astype("str")` Nos ayuda a cambiar el tipo de dato

Cuando tenemos un carácter que nos impide cambiar el tipo de datos podemos eliminarlo así pero funciona solo si es un `int`

```python
# eliminamos el $
df["phone"] = df["phone"].str.strip("$")
# cambiamos el tipo de dato de la columna telefono
df["phone"] = df["phone"].astype("int")

# verificamos que el tipo de dato cambiara

assert df["type"].dtypes == "int" 
```

### Datos categoricos

Ejemplo: 
![[Pasted image 20240327103548.png]]
- Son `int` pero no podemos hacerlo así podríamos tener análisis erróneos lo mejor es cambiar el tipo de dato a `category`

### Datos dentro de un rango
cuando tenemos un rango de datos pero por errores humanos agregan rangos que no.
- Afecta a rangos de fecha por que podemos tener fechas futuras que no an pasado
#### Manejar datos fuera del rango
- Eliminar los datos
	- ![[Pasted image 20240327111910.png]]

- Establecer minimos o maximos personalizados para sus columnas
- configurar los datos como perdidos o [[imputarlos]]
- asignar un valor personalizado para cualquier valor de nuestros datos