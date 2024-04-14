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
## Agrupar datos

La orden de ejecución es diferente cuando se ORDENA:
1. `FROM`
2. `GROUP BY`
3. `SELECT`
4. `ORDER BY`
5. `LIMIT` 

>[!tip] GROUP BY
`GROUP BY` Nos permite agrupar y debe de estar unida con funciones de agregación


>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT certification
>FROM films
>GROUP BY certification;
>```
>En una columna me va a mostrar todos los grupos de certificación

Podemos agregar mas campos en el group by

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT certification, language, COUNT(title)
>FROM films
>GROUP BY certification;
>```
>Se van a agrupar mediante grupos de las dos columnas

Lo podemos combinar con [[ORDER BY]]

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT certification, language, COUNT(title) as title
>FROM films
>GROUP BY certification;
>ORDER BY title
>```
>La funcion agregada tambien agarra en el AS para traerlo a order by

## group by con [[FUNCIONES Y OPERADORES]]

```sql
select
	substring(email,position('@' in email)+1) as domain,
	count(*)
from users u
group by substring(email,position('@' in email)+1)
having count(*) > 1;
```
