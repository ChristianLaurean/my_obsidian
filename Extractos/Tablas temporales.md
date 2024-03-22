---
Author: You Tube
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
1. **CREATE TABLE**: Esta parte de la consulta se encarga de crear una nueva tabla en la base de datos.
    
2. **#tabla_temporal**: `#` indica que esta es una tabla temporal.**Las tablas temporales son tablas que existen solo durante la sesión de la base de datos y se eliminan automáticamente cuando la sesión termina.**
    
```SQL
CREATE temporary TABLE if not exists tabla_temporal (
    columna1 INT,
    columna2 VARCHAR(50),
    columna3 DATE
);
```

Son utilizadas para crear [[Stored Procedures]]
