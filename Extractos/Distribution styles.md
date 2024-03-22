---
Author: Coderhouse
Category: Bases de datos
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---
Debemos de distribuir los datos de manera eficiente en cada nodo de un [[Clustering]] o [[MPP]] y lo hacemos con Distribution styles.

# Tipos de distribucción
- Even
	- Los datos se van a distribuir equitativamente a través de todos los nodos
- Key
	- El nodo lider nos va a ayudar a segmentar o agrupar los registros con un valor en especifico en un nodo.
	- Es ventajoso cuando una tabla se consulta frecuentemente.
	- se agrega en una columna cuando se hacer un [[Joins]]
- All
	- Es todo, toda la tabla en un nodo. Cuando tenemos una tabla que casi no se consulta.
- Auto
	- automáticamente se escoge uno de los 3 anteriores para ver cual es el mas optimo. 

# Claves para aumentar el desempeño de una tabla

## Distribution Key
- Actúa con el estilo de distribución para saber que registros van con que nodos
- ![[Pasted image 20240307103823.png]]
- Cuando tenemos una Diskey pensamos en categorías
## Sort Key

Determina como se van a guardar los registros de forma fisica. y nos ayuda a ordernar
- Si quieres guardar de manera física por una fecha solo ponemos esa columna.
![[Pasted image 20240307104003.png]]


- **Distkey: distribuye para el procesamiento en paralelo**

- **Sort key: determina en que orden se almacenan los datos.**