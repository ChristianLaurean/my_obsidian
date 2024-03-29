---
Author: DataCAMP
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# CTE

Sirven para mejorar la legibilidad y accesibilidad de la información en las [[subquerys correlacionadas]] 

```SQL 
WITH cte as (
	SELECT col1, col2
	FROM table)

SELECT 
	avg(col1) AS a
FROM cte;
```

### si tenemos varias subcolsultas podemos hacerle asi: 
![[Pasted image 20240123103222.png]]
**CTE se ejecuta y se almacena en memoria**.

Si tengo 2 CTE puedo usar el CTE 1 para recuperar su información.

## CTE recursivo
