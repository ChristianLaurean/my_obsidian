---
aliases:
  - Vistas
  - Vistas en Bases de datos
---
## ¿Qué son las [[280 - Vistas no materializada|Vistas]]

>[!tip] Definición
> Es una tabla virtual que no pertenece al [[244 - Schemas|Schemas]]

>[!quote] Tener en cuenta
> - No se almacena en la memoria física
> - Los datos de la vista provienen de una consulta de la tabla de una [[1 - Bases de datos|Base de datos]]
> - Las vistas son utiles mas alla de la [[8 - 2FN|2NF]]
> - Lo mejor es solo usar las vistas en modo lectura

## Pro y contras de las vistas 

**Pros**

- No se necesita volver a escribir la [[2 - Querys|Querys]] para consultas recurridas
- Mejora el flujo de trabajo
- Permite agregar tablas virtuales sin dañar el modelo

## Código

>[!example] Codigo [[PostgreSQL]] para crear una [[280 - Vistas no materializada|Vistas]]
>```SQL
>CREATE OR REPLACE VIEW name_view AS 
>SELECT col1, col2
>FROM table_name
>WHERE condition;
>```
>La [[2 - Querys|Querys]] puede ser la que sea

---

>[!example] Codigo [[PostgreSQL]] para [[2 - Querys|Querys]] la [[280 - Vistas no materializada|Vistas]]
>```SQL
>SELECT *
>FROM name_vista;
>```

---

>[!example] Codigo [[PostgreSQL]] para ver todas las [[280 - Vistas no materializada|Vistas]] de la [[1 - Bases de datos|Base de datos]]
>```SQL
>SELECT *
>FROM INFORMATION_SCHEMA.views;
>```

---

>[!example] Codigo [[PostgreSQL]] para excluir vistas del sistema y acceder a los que e creado
>```SQL
>SELECT * FROM INFORMATION_SCHEMA.views
>WHERE table_schema NOT IN ('pg_catalog','information_schema');

---
**Eliminar una fila**

>[!example] Codigo [[PostgreSQL]] Eliminar una [[280 - Vistas no materializada|Vistas]]
>```SQL
DROP VIEW view_name [CASCADE | RESTRICT];

Hay veces que objetos dependen de las vistas y Restrict evita que se elimine la vista si  depende de otras cosas

>[!example] Codigo [[PostgreSQL]] Cambiar una [[280 - Vistas no materializada|Vistas]]
>```SQL
CREATE OR REPLACE VIEW view_name as New_query;

Podemos modificar las propiedades de las vistas

![[Pasted image 20231201112357.png]]
