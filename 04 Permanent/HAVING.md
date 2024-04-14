---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
cssclasses:
  - center-titles
  - page-white
---
## FILTRANDO DATOS AGRUPADOS

La orden de ejecución es diferente cuando se ORDENA:
1. `FROM`
2. `where`
3. `GROUP BY`
5. `HAVING`
6. `SELECT`
7. `ORDER BY`
8. `LIMIT`

`HAVING`

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT certification, language, COUNT(title) as title
>FROM films
>GROUP BY certification;
>HAVING COUNT(title) > 10;
>```
>con having podemos filtrar las agrupaciones

