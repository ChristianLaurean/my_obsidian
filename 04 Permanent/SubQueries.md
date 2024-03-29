---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# conceptos

>[!warning] Es un poder que conlleva mucha responsabilidad
>por que puede afectar el rendimiento de la [[Base de datos]]
>Por que:
>Por que si tuvieramos una tabla de 1 millon de registros entonces el query inicial se va a ejecutar 1 millon de veces para verificar la información y cada registro va a verificar otra vez el millon de registros de la subquery

>[!tip] Subquery
>Es un [[query]] que lleva a otro query y este subquery lo puedes poner en cualquier lado
>```sql
>SELECT
>FROM (
>	query
>) as tabla_nueva;
>Esto es una subquery con el FROM
>```


