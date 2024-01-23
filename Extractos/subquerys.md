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
