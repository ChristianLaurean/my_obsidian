---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---
Se compone de Metricas y [[Dimensiones]]

-  [[Hechos]] esas métricas que queremos medir (los indicadores de nuestro negocio)
- Los atributos están almacenados en nuestras [[Dimensiones]] osea son las perspectivas por las que quiero ver esas métricas.  

Tabla de [[Hechos]] o Fat donde tenemos todas las métricas del negocio y las dimensiones que son las diferentes perceptivas de las métricas

![[Pasted image 20240208101046.png]]

# 4 Componentes para crear un modelado dimensional
1. Definir a qué proceso de negocio estamos haciendo referencia 
	- Por ejemplo para una empresa de ventas el proceso que debemos de darle referencia es a las **Ventas
2. [[Grain]]
	1. Es que tan especifico deben de estar los datos almacenados en la tabla de [[Hechos]].
	2. Debemos de tener una granularidad que no se puedan dividir mas los datos. 
	- Album de musica < canción individual
	- Servicios individuales > servicios generales
4. Identificar las [[Dimensiones]] 
	- Donde se hacen mas ventas
	- ¿nombre del vendedor con mas ventas?
	- Comunmente se utilizan estos:
		- Tiempo: Year, cuatrimestre,mes
		- Localización: Addres, estado y ciudad
		- Usuarios: nombre, Emails,direccion
1. Identificar los [[Hechos]]
	1. Identificar los hechos numericos que llenaremos cada fila de la tabla 

>[! Danger] Nunca se relacionan dos tablas de [[Hechos]]