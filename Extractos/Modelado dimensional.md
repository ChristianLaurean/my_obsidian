---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---

# identificar las preguntas de negocio

Son todas las necesidades que tiene nuestro cliente o nuestro usuario del negocio que se pueda resolver mediante [[Datos]] 
- "Entre mas preguntas negocio nos hagamos en nuestro sistema mejor sera nuestro [[Extractos/Modelado dimensional|Modelado dimensional]]"
2. identificar los [[hechos]] y las [[Dimensiones]] mediante las preguntas de negocio
	1. Unidades vendidas de cada producto por cliente en un tiempo determinado
		1. Unidades vendidas- hechos
		2. Producto - Dimensión
		3. Cliente - Dimensión
		4. Date - Dimensión
3. Identificar las **reglas de negocio** 
4. Crear un modelado dimensional
	1. Crearemos los diagramas.
	2. Creamos las dimensiones primero
	3. No es necesario relacionar las tablas con la de hechos Por qué una dimensión puede usarse en otros [[Extractos/Modelado dimensional|Modelado dimensional]] 
