---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
## Filtrar datos con [[2 - Querys|Querys]]

**La orden de execución es diferente cuando se filta ahora es:**
1. `FROM`
2. `WHERE`
3. `SELECT`
4. `LIMIT`

>[!tip] Como filtramos
`WHERE` Nos ayuda a filtrar datos de la base de datos

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
SELECT names
FROM empleos
>WHERE year > 25
>LIMIT 10;

### Filtrar con múltiples criterios

`OR` Es esto O esto 
`AND` Es Esto y Esto = True

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
select *
>from films f
>where (duration >= 50 and duration <= 100) and (certificacion = 'PG' or certificacion = 'R');

`BETWEEN` Muéstrame Entre este numero y el otro

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
SELECT names
FROM empleos
>WHERE year 
>	BETWEEN 1992 AND 2000;

### Filtrar Texto

>[!tip] Filtrando texto
`LIKE` Lo usamos para encontrar un petron
>	`%` Concide con 0, uno o muchos caracteres de texto
	
	
>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE name LIKE 'Adel%'
>
>
>SELECT *
>
>FROM users
>
>WHERE name LIKE 'Jim %';-- También podemos buscar con espacios
>
>```
>Busca los nombres que empiecen con Adel

`_`

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE name LIKE 'Adel_'
>```
>Solo me trae los que empiecen con un solo caracter

`NOT LIKE` Busca los patrones que no coincidan

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE name NOT LIKE 'Adel%'
>```
>Te trae todos excepto los que empiezan con Adel

`IN`

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE year IN (1990,1996,1997)
>```
>nos trae los registros de todas esas fechas

## filtrar valores [[258 - Datos NULL|NULL]]

`IS NULL`

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE year IS NULL;
>```
>Filtra los valores que son null

`IS NOT NULL`

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT names
>FROM empleos
>WHERE year IIS NOT NULL;
>```
>Filtra los resultados que no sean null
