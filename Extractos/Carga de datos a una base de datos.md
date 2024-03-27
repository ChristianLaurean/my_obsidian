---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
---
# Cargar datos a una [[Base de datos]] [[PostgreSQL]]


```
# creamos una conecxion 
df .sql(nombre_tabla,db_engine)
```

**Paramatros**
- name: nombre de la tabla
- con=db_engine
- if_exists= "append" o "replace"
- index= true o False si se va a cargar el indice a la base de datos
- index_label= "nombre de una columna"
# validación de datos
- recuentos concidan entre los datos trasformados y datos persistentes 
- Validad que cada fila éste presente en ambos DF