---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# Código para crear una tabla


>[!example] [[PostgreSQL]]
```SQL
CREATE TABLE "nombre_tabla" (
	id SERIAL,
	columna VARCHAR(100) NOT NULL,
	PRIMARY KEY(id)
);
```


## Agregar varias [[2 - Primary Key|Primary Key]] en una tabla

>[!example] [[PostgreSQL]]
>```SQL
>CREATE TABLE table_name (
>	id_colum INTEGER,
>	id_colum_a INTEGER,
>	colum_b VARCHAR,
>	PRIMARY KEY (id_colum, id_colum_a)
>);

>[!warning] Evita usar muchos atributos para la [[2 - Primary Key|Primary Key]]
>Las [[2 - Primary Key|Primary Key]] constan de la menor cantidad posible de columnas posible!


## Como crear una tabla con [[7 - Clave Foranea|Foreing Key]]

>[!example] [[PostgreSQL]]
>```SQL
>CREATE TABLE table_name (
>	id_colum INTEGER PRIMARY KEY,
>	id_colum_a INTEGER REFERENCES name_table_2 (colum_id2);

>[!warning] Recuerda primero hacer las tablas que no tengan [[7 - Clave Foranea|Foreing Key]]
> Así no evitaremos problemas al crear las tablas


## ¿Como agregar un consistencia en los [[3 - Constraints|Constraints]]''

>[!example] [[PostgreSQL]]
>```SQL
>CREATE TABLE table_name (
>	id_colum INTEGER PRIMARY KEY,
>	id_colum_a INTEGER REFERENCES name_table_2 (colum_id2) ON DELETE NO ACTION);

- **ON DELETE NO ACTION** : Si se eliminar un registro en la tabla b entonces va arreojar un error.
- **ON DELETE CASCADE**: Se elimina los registros de las dos tablas 
- **ON DELETE RESTRICT**: Evita que elimines un registro
- **ON DELETE SET NULL**: se agrega un valor [[258 - Datos NULL|NULL]]
- **ON DELETE SET DEFAULT**: Se agrega un valor por defecto