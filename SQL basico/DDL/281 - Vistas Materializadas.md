---
aliases:
  - Vista Materializada
---
## ¿Qué es una [[281 - Vistas Materializadas]]?

>[!tip] Definición
>Es lo mismo que una [[280 - Vistas no materializada|Vistas]]
> Se materializan físicamente mientras que las otras permanecen virtuales
> - Almacena los resultados de la consulta en el [[Disco duro]]
> - Se actualizan solas cuando las llamas
 > - Son excelentes si tienes consultas con un tiempo de ejecución prolongado
 > - Permiten [[2 - Querys|Querys]] de consultas largas y obtener resultados muy rápidamente
> - Los datos se quedan como la ultima vez que la actualizaste
> - Son útiles para [[264 - Data Warehousing|Data Warehousing]]

>[!Warning]  No usar vistas si los datos se actualizan constantemente
>Por ejemplo para [[1 - Bases de datos|Bases de datos]] [[262 - OLTP|OLTP]]

## código

>[!example] Codigo [[PostgreSQL]] para crear [[281 - Vistas Materializadas]]
>```SQL
CREATE MATERIALIZED VIEW mi_mv AS query;
>```

>[!example] Codigo [[PostgreSQL]] para actualizar [[281 - Vistas Materializadas|Vista Materializada]]
>```SQL
>REFRESH MATERIALIZED VIEW my_mv;


