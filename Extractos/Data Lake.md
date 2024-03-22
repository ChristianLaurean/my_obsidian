---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Diseño de bases de datos|Diseño de bases de datos]]"
---
Es un repositorio donde nos permitirá almacenar información 
- Estructurada
- Semis-estructurada
- No estructurada. Son imagenes, fotos
Pero son archivos sin procesar


Las ventaja 
- nos permitirá hacer análisis a todo tipo de información 
- A una gran velocidad
- Nos permitirá hacer procesos de [[Streamings]]

![[Pasted image 20240208084134.png]]

Normalmente se usan [[S3]] de [[AWS]] o [[Storage]]

## Schema on read
Se crea un Schema cuando queremos leer un archivo. osea que como no tenemos una estructura gracias al Schema on read nos sirve para saber que tipo de estructura quiero que sea mi archivo.

>[!warning] Los Data Lakes tienen un costo ALTO!!!

>[!tip] Los Data science están mas en los [[Data lakes]]

>[!warning] Para Procesar los datos se puede durar Semanas a Meses

