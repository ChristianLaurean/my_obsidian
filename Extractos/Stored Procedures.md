---
Author: You Tube
Category: SQL
Type: Video
Status: Terminado
relación: "[[Curso de SQL]]"
---
Es un grupo de declaraciones SQL que sea han creado y luego se han almacenados en esa [[Base de datos]] puede aceptar parámetros de entrada 

# Creación procedimiento

```SQL
create or replace procedure prueba()
language sql
as $$
	select * from doctors
$$;

-- Llamamos al procedimiento
call prueba();
```

[[Creación de Tablas]]
# ETL EJEMPLO

```SQL

create or replace procedure prueba()
language plpgsql
as $$
begin
	drop table if exists temp_table;


	create temporary table if not exists temp_table (
		id INT,
		name VARCHAR(50),
		speciality varchar(100),
		hospital varchar(50),
		city varchar(50),
		consultation_fee int4
		);
  

	insert into temp_table
	select * from doctors;


end;
$$;

  
call prueba();
select * from temp_table;

```

**Parámetros:**

Puedes agregar parámetros al procedimiento almacenado para hacerlo más flexible y reutilizable.

```SQL
CREATE OR REPLACE PROCEDURE nombre_procedimiento(param1 tipo1, param2 tipo2)
LANGUAGE plpgsql
AS
$$
BEGIN
   -- Instrucciones SQL usando param1 y param2
END;
$$;
```
