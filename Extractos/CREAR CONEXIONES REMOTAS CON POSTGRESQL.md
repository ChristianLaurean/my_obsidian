---
Author: Christian laurean
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
```sql
CREATE EXTENSION IF NOT EXISTS postgres_fdw;

-- Crear el servidor FDW
CREATE SERVER IF NOT EXISTS conn_db
	FOREIGN DATA WRAPPER postgres_fdw
	OPTIONS (dbname 'DESASTRES', host 'localhost', port '5432');

  

-- Crear el mapeo de usuario

CREATE USER MAPPING IF NOT EXISTS FOR CURRENT_USER
	SERVER conn_db
	OPTIONS (user 'chris', password 'Milito21');

-- Creamos un schema donde extraemos las tablas que tiene la otra base de datos

CREATE SCHEMA IF NOT EXISTS remote_schema;

-- Importar tabla remota

IMPORT FOREIGN SCHEMA public
FROM SERVER conn_db
INTO remote_schema;

-- eliminamos el schema
DROP SCHEMA IF EXISTS remote_schema CASCADE;

-- eliminamos la extension

DROP EXTENSION IF EXISTS postgres_fdw CASCADE;
```