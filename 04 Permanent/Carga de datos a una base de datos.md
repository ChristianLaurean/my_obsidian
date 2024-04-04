---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - center-titles
  - page-white
  - pen-black
---
# Consideración a la hora de cargar los datos.

- Que formatos son aceptables en nuestro [[Target]]
- **Permisos** Siempre debemos tener permisos de escritura en nuestro [[Target]]
- **Auditar**: Comparar los datos de referencia por que permite  detectar errores, problemas de calidad y duplicados en el proceso.
- **Eficiencia** Debes Buscar la manera mas eficiente de extraer y cargar los datos para evitar retrasos y errores
- **Control de Errores** Es importante establecer un plan de acción en caso de presentarse un error¿deberíamos de repetir todo el proceso o solo corregir los fallos y continuar con el proceso?
# Cargar datos a una [[Base de datos]] [[PostgreSQL]]



```python
# creamos una conecxion 
df.sql(nombre_tabla,db_engine)
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