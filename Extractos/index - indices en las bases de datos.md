---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
>[!tip] indices
>Los indices funcionan para decirle a la base de datos que se prepare por que voy a hacer búsquedas con ese indice 
>- Mejora la velocidad de la base de datos

### Creando indices
Cada indice toma como referencia el tamaño de la base de datos, entre mas grande mas [[Ram|Memoria]] va a requerir
- Si haces el indice ya  cuando la [[Base de datos]] esta muy grande va a tomar su tiempo en crearse.
 - Se pueden crear indices compuestos si sabemos que las dos columnas son valores únicos. 

```sql
# Para columnas unicas
CREATE UNIQUE index "unique_table_name" on nombre_tabla(name_column);

# index 
CREATE index "table_name" on nombre_tabla(name_column)
```