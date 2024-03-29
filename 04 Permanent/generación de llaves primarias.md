---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# Serial vs identity

`Serial`:Sirve para crear llaves primarias que son int y not null y unique.

>[! Danger] Puede crear [[Anomalías de insersión]] 
>Por que como es cor-relacionado y si se agregan números de forma manual podría generar muchos errores a futuro. 
### Ejemplo

```SQL
CREATE TABLE name_table (
	id serial primary key,
	dato, varchar
)
```


Es lo mismo solo que te permite mas manipularlo y que no se agreguen manualmente

```SQL
CREATE TABLE name_table (
	id INTEGER GENERATED ALWAYS AS identity PRIMERY KEY,
	dato, varchar
);


-- id que empiece en 100 y se incremente en 2 en 2
CREATE TABLE name_table (
	id INTEGER GENERATED ALWAYS AS IDENTITY (START WITH 100 INCREMENT BY 2),
	dato, varchar
);
```

# Primary key [[Keys - Llaves|llave compuesta]] 

```SQL
CREATE TABLE name_table (
	id int,
	id2 int,
	PRIMARY KEY (id,id2)
);
```



# UUIDS

```SQL
DROP EXTENSION "uuid-ossp";
-- instalar
CREATE EXTENSION IF NOT EXISTS "uuid-ossp";


CREATE TABLE name_table (
	id uuid DEFAULT gen_random_uuid(),
	PRIMARY KEY (id)
);
```

##  ejemplo
![[Pasted image 20240117072830.png]]

# Secuencias

Es otra forma de generar primarys keys

```sql
CREATE SEQUENCE nombre_secuencia;

CREATE TABLE name_table (
	id INTEGER PRIMARY KEY DEFAULT nextval('nombre_secuencia')
);
