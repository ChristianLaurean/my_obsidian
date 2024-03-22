---
Author: DataCAMP
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---
# El almacenamiento de columnas es mejor para Consultas analíticas[[OLAP]]

Normalmente las computadoras almacenan datos en bloques en [[Almacenamiento|disco duro]]
![[Pasted image 20240216095309.png]]
- Los datos almacenados en muchos bloques tardan mas en recuperarse que en menos bloques. 
- Debemos de almacenar los datos en pocos bloques para aumentar las velocidades de las consultas

### Almacenamiento en Columnas

Almacena los datos de una columna juntos
Ejemplo:
![[Pasted image 20240216101815.png]]
- Ahora los datos de la columna se almacenan juntos a un solo bloque osea por cada columna seria un bloque nuevo.
- Esto hace que las consultas sean mas rápidas por que tenemos menos bloques que buscar. 
>[! warning] Desventaja
>Es que a la hora de insertar datos el disco duro necesita leer todo el bloque y editarse y eso hace que sea muy lento [[INSERT|Insertar]] los datos

### Almacenamiento de filas

Las filas se almacenan en un bloque en nuestro disco duro.
Sirve mucho para las [[OLTP]]

Por que en las querys el disco duro tiene que buscar por cada bloque y  como lo vimos arriba entre mas bloques, mas tarda en recuperar la data.

Ejemplo:
![[Pasted image 20240216101358.png]]