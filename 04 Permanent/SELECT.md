---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
## ¿Como se ejecuta el código de [[1 - SQL|SQL]]?

Como en la [[programación]] el código no se procesa en el orden que se escribe.

1. `FROM` es lo primero que busca para saber en que tabla ir a buscar
2. `SELECT`
3. `where` Después se filtra
4. `LIMIT`se limitan los datos

## **[[2 - Querys|Querys]] Basico**

- `SELECT` Es una palabra clave que nos ayuda a traer cualquier columna de la base de datos.
- `FROM` Le damos a indicar en que tabla se encuentran los datos que queremos ver con el `SELECT`
- `AS` Nos sirve para cambiar el nombre del campo.
- `DISTINCT` Nos sirve para que los datos no salgan repetidos y solo los únicos.

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
SELECT DISTINCT names AS nombres
FROM empleos;
