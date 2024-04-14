---
Author: DataCAMP
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
Realizan cálculos en un conjunto de resultados que ya se an generado y son utilizado para hacer [[¿Cuales son las Funciones agregadas en SQL?]] sin utilizar [[GROUP BY]]

```sql
SELECT
	date,
	columnas,
	AVG(columns) OVER() AS overall_avg
FROM tabl;
```

# GENERATE RANK

crea una numeración de columnas de mayor a menor o de menor a mayor en funcion de la columna que le des. 

```sql
SELECT
	date,
	columnas,
	RANK() OVER(ORDERBY columns DESC) AS overall_avg
FROM tabl;
```

>[!WARNING] Consideraciones
>- Se procesan después de la consulta completa excepto ORDER BY

# PARTITIONS

Nos permite calcular valores separados para diferentes categorías establecidas en la partición 

`AVG(column) OVER(PARTITION BY columna_se_va_dividir_promedio)
podemo poner las columnas que queramos dividir

![[Pasted image 20240123111952.png]]

# sliding windows

Estos hacen cálculos en las filas del conjunto de datos

`ROWS BETWEEN star AND finish`
 en star y finissh se utiliza estas funciones: 
 `PRECEDING` Para especificar el numero de filas antes o despues de un calculo.
 `FOLLOWING`
 `UNBOUNDED PRECEDING`
 `UNBOUNDED FOLLOWING` desea incluir el principio y el final de los calculos
 `CURRENT ROW` detener su calculo en la fila actual
![[Pasted image 20240123112737.png]]

# row number 

```SQL
select row_number() over() as row_id,*
from platzi.alumnos;
```

`row_number`:traerme el numero de registro
`over()` Todas las columnas