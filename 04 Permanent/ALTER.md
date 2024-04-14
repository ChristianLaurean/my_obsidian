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


## ¿Cómo cambiar el nombre de la tabla?

>[!example] Cambiando el nombre de la tabla
>```SQL
>ALTER TABLE table_name
>RENAME COLUMN old_name TO new_name;

## ¿Cómo cambiar el tipo de dato de la columna?

Esto suele pasar cuando nos equivocamos a la hora de [[251 - Creación de tablas|Creación de tablas]] y esta forma lo podemos resolver

>[!example] Cambiar el [[4 - Tipos de datos|Tipos de datos]]
>```SQL
>ALTER TABLE table_name
>ALTER COLUMN columname
>TYPE varchar(128); 

La mayoria de las veces no funciona y para eso le agregamos esto: `USING columna::tipo_dato;`

## ¿Cómo eliminar una columna de la tabla?

>[!danger] Eliminar columnas
>```SQL
>ALTER TABLE table_name
>DROP COLUMN column_name;

>[!danger] Eliminar [[CONSTRAINS]]
>```SQL
>ALTER TABLE table_name
>DROP CONSTRAINT "nombre_constraint";
## ¿Cómo agregar not null a una columna?

>[!example] Agregar NOT [[258 - Datos NULL|NULL]]
>```SQL
>ALTER TABLE table_name
>ALTER COLUMN columname
>SET NOT NULL;

## ¿Cómo eliminar Not [[258 - Datos NULL]]?

>[!example] Eliminar [[3 - Constraints|Constraints]]
>```SQL
>ALTER TABLE table_name
>ALTER COLUMN columname
>DROP NOT NULL;

## ¿Cómo agregar unique o un [[3 - Constraints|Constraints]]?

>[!example] Agregar [[3 - Constraints|Constraints]]
>```SQL
>ALTER TABLE table_name
>ADD UNIQUE(column_name);

# [[2 - Primary Key|Primary Key]]

>[!example] Agregar [[3 - Constraints|Constraints]]
>```SQL
>ALTER TABLE table_name
>ADD PRIMARY KEY(column_name);

# [[7 - Clave Foranea|Foreing Key]]

>[!example] Agregar [[3 - Constraints|Constraints]]
>```SQL
>ALTER TABLE table_name
>ADD FOREIGN KEY (column_name) REFERENCES b (id);

# Agregar un nuevo atributo combinando dos atributos o hacer un

>[!example] Agregar [[3 - Constraints|Constraints]]
>```SQL
>ALTER TABLE table_name
>ADD COLUMN column_c Varchar()
>UPDATE table_name
>SET column_c = CONCAT(column_a, column_b);



