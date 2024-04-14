---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
cssclasses:
  - center-images
  - center-titles
  - page-white
---
## Ordenar los datos

La orden de ejecución es diferente cuando se **ORDENA**:
1. `FROM`
2. `WHERE`
3. `SELECT`
4. `ORDER BY`
5. `LIMIT` 

>[!tip] ORDER BY
`ORDER BY` Nos sirve para ordenar nuestros datos de una columna o de otra de formar Ascendente y descendente 
`ASC` De Menor a mayor o de A a la Z
`DESC` De mayor a menor de la Z a la A

### Se puede ordenar por varios campos

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE year IS NOT NULL
>ORDER BY year, names
>```
>Primero se van a ordenar los años y despues los nombres

