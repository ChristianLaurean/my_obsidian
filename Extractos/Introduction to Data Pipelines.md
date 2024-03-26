---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
---
Una `Pipeline` Es un proceso automatizado que extrae datos de un sistema fuente y los trasforma en un modelo deseado y carga los datos trasformados en un archivo, [[Base de datos]] o un [[Data Warehouse]].
![[Pasted image 20240325150948.png]]


# Diseño de un data pipeline

[[ETL]]
[[ELT]]

**Antes de empezar con un proyecto de pipeline lo mejor es empezar hacer un diseño de arquitectura**
En el proceso de diseño se ve:
- exploran y documentan como se crean los datos en los sources incluido el formato y el método de entrega y la frecuencia.
- Determinar la complejidad de las trasformaciones 

Es importante que el proceso sea
- resiliente: Maneja Fallas y Errores
- idempotentes: Si se ejecuta varias veces el resultado debe de ser el mismo y no debe de dar duplicados.
- escalable: Manejan grandes cantidades de datos, y una mayor frecuencia de ejecución.
- trasparente:Evitan operaciones de caja negra con los datos y están bien probados y documentados.
# caracteristicas importantes

- **Persistencia de los datos.**
	- Es importante capturar múltiples "instantaceas" de los datos a medida que atraviesan la pipeline
	- ![[Pasted image 20240326091441.png]]
	- El almacenamiento de datos en un archivo u otro medio de almacenamiento se conoce como persistencia de datos.
	- Los archivos verdes muestran lugares lógicos para conservar datos dentro de la pipeline
	- El pipeline puede volverse a ejecutar desde el ultimo punto de la falla y en lugar de empezar al inicio
	- LA persistencia de los datos facilita la documentación de las operaciones realizadas
- Data Lineage
	- Es la practica de documentar el viaje de esos datos a travez del pipeline
	- proporciona trasparencia y hay confienza en los cunsumidores
- Antes de pasarla a producción
	- Hacer pruebas unitarias
	- debe probarse de un extremo a otro, utilizando pequelos como grandes archivos vacios o incluso datos incorrectos.
	- El codigo debe de ser revisado antes de procución