---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# operadores de Strings y funciones

`||` **cibcatena dos o mas strings**

`CONCAT()`: UNE DOS O MAS STRINGS

`LOWER()`: En misnuculas

`UPPER()` EN mayusculas

`LENGTH()` cuenta los caracteres que tiene

```SQL
select
	LOWER(name),
	UPPER(name),
	LENGTH(name),
	20 * 5 as constante,-- podemos hacer la operación que queramos y poner el nombre que queramos
	concat(id,'_', name),
	name || ' ' || id
from users;
```


`SUBSTRING()` Extrae el string de otro [[string]]
`POSITION()` BUSCA EL TERMinación EN EL CAMPO Y RETORNA EL INDICE
`TRIM(TEXT)` Remueve los espacios iniciales y finales del string
```SQL
select
	name,
	substring(name,0,position(' ' in name)) as first_name,#empezamos con 0
	substring(name,position(' ' in name)+1) as last_name #si no ponemos nada es hasta donde tope hueso-- Tambien el +1 es para que no cuente el espacio
from users;
```


### [[UPDATE]] a muchisisismo registros
```sql
update
	users
set
	first_name = substring(name,0,position(' ' in name)),
	last_name = substring(name,position(' ' in name)+1);
```
