---
Author: Coderhouse
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---
# incremental loads

- Hacer cambios sobre filas que ya existen
	- `UPSERT` es la combinación de [[UPDATE]] + [[INSERT]]
		- Cuando la fila ya existe se actualizan los datos
		- Cuando la fila no existe se insertan los datos.
	- Generalmente tenemos una tabla [[Staging]]
		- Soluciones
			- Borrar todas las filas que tenemos en la tabla destino que están presentes en la tabla de [[Staging]] y despues actualizamos la tabla destino con todo lo que tiene [[Staging ETL]]
			- En la tabla destino actualizar todas esas filas que tienen concidencias y regresamos a la tabla staging y las borramos y las filas que quedan las insertamos en la tabla destino.
- Ejemplo con SQL
```SQL
begin transaction;
delete from tabla  using tabla_staging --Elimina todo lo que concida con ambas tablas
where tabla.id=tabla_staging.id and tabla.insert_date>='date'; --condiciones cual podemos hacer este delete
insert into tabla select * from tabla_staging;
end transaction;