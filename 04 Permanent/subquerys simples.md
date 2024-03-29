---
Author: You Tube
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
Es una consulta anidada dentro de otra consulta. 

```SQL
SELECT column
FROM (SELECT column
	 FROM table) AS subquery;
```

- Se pueden colocar en cualquier lugar de la query
`SELECT` `FROM`  `WHERE` `GROUP BY`

# SUBQUERY SIMPLE

Es una subquery, anidada dentro de otra consulta, que se puede ejecutar por si sola..

```sql
SELECT column
FROM table
WHERE comlum > (
	SELECT AVG(column)
	FROM table
)
```

- Primero procesa toda la información dentro de la subconsulta y luego pasa la información en la consulta externa y la consulta externa usara esos datos
## Subconsultas con el where

- Son utiles para filtrar resultados segun la información.
- Es util por que no se pueden usar [[Funciones agregadas]] en el [[WHERE]]
#### lista de filtrado

```sql
SELECT column
FROM table
WHERE comlum IN (
	SELECT column
	FROM table_2
)
```

## subconsultas con from

- Es una herramienta robusta para reestructurar y transformar datos

![[Pasted image 20240122092822.png]]

### subquerys con [[SELECT]]

- Sirven para traer valores resumen aun conjunto de datos detallado.
>[!warning] Recuerda que no se puede poner na [[Funciones agregadas]] con un [[GROUP BY]] 

```sql
SELECT 
	column
	COUNT(id) 
	(SELECT COUNT(id) FROM table) AS total_table
FROM table
GROUP BY season;
```

- Son útiles para realizar cálculos matemáticos complejos 

```sql
SELECT 
	column
	(columna1 + columna2) AS col,
	(columna1 + columna2) - (SELECT AVG(id) FROM table) AS total_table
	
FROM table
GROUP BY season;
```
#### CONSIDERACIONES AL USAR SUBQUERYS CON SELECTS

>[!warning] consideraciones
>1. La subconsulta debe devolver un unico valor
>2. Colocación correcta de la subquery - la subquery se procesa antes de la principal

# mejores practicas

Ejemplo superquery

![[Pasted image 20240123094854.png]]

1. Formatear corretamente la query
2. Agregar comentarios
	1. ![[Pasted image 20240123095102.png]]
	2. Escribir lo que hace la consulta
	3. Comentarios entre lineas 
		1. ![[Pasted image 20240123095150.png]]
3. Asegurarme de agregarle ident 
	1. con el [[CASE - THEN]] ![[Pasted image 20240123095331.png]]
# responden preguntas

- Son excelentes para hacer coincidir datos de diferentes columnas en uno o mas tablas y responde a:
- Quien es el supervisor inmediato de cada empleado. 