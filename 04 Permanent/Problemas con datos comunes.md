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
Cuando tenemos un rango de datos pero por errores humanos agregan rangos que no.
- Afecta a rangos de fecha por que podemos tener fechas futuras que no an pasado
- Lo convertimos la columna a tipo de dato de fecha![[Pasted image 20240328090842.png]]
- ![[Pasted image 20240328091056.png]]

#### Manejar datos fuera del rango
- Eliminar los datos
	- Solo cuando hay una pequeña proporción de los datos estén fuera del rango
	- ![[Pasted image 20240327111910.png]]

- Establecer minimos o maximos personalizados para sus columnas
- configurar los datos como perdidos o [[imputarlos]]
- asignar un valor personalizado para cualquier valor de nuestros datos

# Valores duplicados

Esto pasa cuando tenemos registros que son exactamente iguales.

Pasos para manejar datos duplicados

1. Encontrar valores duplicados
	1. `.duplicated()` Devuelve una serie de True o False
	2. Parametros
		1. `subset` nos permite pasarle una lista de las columnas
		2. `Keep` nos permite mantener la primera ocurrencia de un valor duplicado por `first`, `last` o `all`
	3. ![[Pasted image 20240328092700.png]]
	4. Tambien podemos ordenarlo con `.sort_values(by="column")`
**Duplicados completos**
- Es cuando tenemos un registro es exactamente igual en todas sus columnas.
![[Pasted image 20240328093111.png]]
- Solo eliminamos un registro y listo
- `.drop_duplicates()` tiene los mismos parametros que `duplicaed()`
**Duplicados incompletos**
- Es cuando tenemos un registro exactamente igual pero tal vez una columna sea diferente.
![[Pasted image 20240328093131.png]]
- Solución Es combinar las dos filas con una medida estadística.  
- ![[Pasted image 20240328094747.png]]
- 