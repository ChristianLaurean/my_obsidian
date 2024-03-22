---
Author: Coderhouse
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---

# Retos de la vida real de querys lentas

- Alguien ejecutando un proceso [[Batch]] y lleva ejecutándose toda la noche y no sabe por que tarda tanto
- Alguien ejecutando una query y no le trae datos.

# ejemplo de querys malas.

![[Pasted image 20240307090622.png]]
1. Mejorar la legibilidad del código 
	1. joins en la misma linea 
	2. Usar alias
	3. ![[Pasted image 20240307091948.png]]
2. Optimizanción del código
	1. Hay inners y left que hace 2 consultas a la misma tabla, lo mejor es solo hacer una usamos AND 
	2. ![[Pasted image 20240307092425.png]]
3. Ver que inners si se esten usando en el [[SELECT]]
	1. Vemos que varios no se están usando para nada.
	2. ![[Pasted image 20240307092629.png]]
4. Cuando tenemos un problema con el input o Output o de procesamiento.
	1. Lo mejor es dividir las consultas mas grandes en consultas mas pequeñas
	2. Buena practica empezar con la tabla mas grande y después las mas pequeñas.
	3. Podemos poner filtros en los joins
	4. ![[Pasted image 20240307094824.png]]
5. Para consultas mas usadas, se puede usar vista indexadas para agilizar el acceso constate a datos importantes
6. 

## Consejos básicos de Querys optimizadas

1. Evitar el * y solo usar las columnas que queremos usar.
2. Evitar el uso de joins excesivos
3. Aplicar filtros de fechas (si es posible)
4. añadir indices
5. Evita usar muchos or
6. Usar Wildcards solo al final para filtros de strings con like
7. Evita hacer muchos select distinct
8. Usar [[LIMIT Y OFFSET]]
9. Evita crear joins con where
10. minimizar operaciones grandes de escritura.