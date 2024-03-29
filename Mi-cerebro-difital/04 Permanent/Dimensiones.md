---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---

- Las dimensiones son el contexto de los [[Hechos]]
- Describen los procesos del negocio y responde las preguntas del negocio ¿Quién?, ¿Qué?,¿Cómo?,¿Cuándo?,¿Dónde?.

Nos van a ayudar a analizar [[Hechos]] en diferentes perceptivas

![[Pasted image 20240208101808.png]]

Una dimensión esta compuesta por atributos 
- Jerárquicos
	- Permiten ir de lo general a lo particular.
	- Consolidar y desagregar. por ejemplo pais
- Descriptivos
	- Información relevante. Netamente descriptiva estos atributos describe las características del elemento de manera directa.. **Por ejem: direccion,Telefono,Talla,clima**
- De control
	- No pertenecen al conocimiento del negocio. **Nos sirven para dar auditoria de nuestros datos** por ejemplo fecha de carga. quien lo hizo y cuando. 