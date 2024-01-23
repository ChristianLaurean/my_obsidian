---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
## ¿Cómo insertar datos a una tabla existente?

>[!tip] INSERT INTO
>```SQL
>INSERT INTO name_table (column1, columns2) VALUES (datos1, datos2);

## ¿Cómo insertar datos de una tabla a otra que ya existe?

>[!tip] INSERT INTO
>```SQL
>INSERT INTO name_table 
>SELECT DISTINCT columns, columns
>FROM table_name_2;


>[!warning] Pedir un respaldo antes de hacer esto.
>```sql
>update country c
>set continent = (select b.code from continent b where b.name = c.continent);
>```

