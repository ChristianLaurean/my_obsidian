---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Diseño de bases de datos|Diseño de bases de datos]]"
---
 
# ¿Que es un Data Warehouse?

>[! tip] DWH
>Es una [[Base de datos]] centralizada que almacena grandes volúmenes de datos de diferentes fuentes.
 
# Que diferencian un Data Warehouse a otras bases de datos?

1. Son excelentes almacenando grandes cantidades de datos
2. Cuentan con herramientas para que las consultas sean eficientes 
3. Pueden convivir varios tipos de datos de diferentes fuentes de información pero se encuentran estructurados
	1. ![[Pasted image 20240124090606.png]]
4. Son de tipo [[OLAP]]
5. Data warehousing tiene datos de diferentes fuentes y todo se encuentra Centralizado
6. Tiene una estructura planificada: La estructura se define mediante la escritura
## Para que nos sirve que los datos estén centralizados?

1. Nos ayuda a responder preguntas y tomar decisiones con los datos.

## querys que se usan

- Deben de ser querys que respondan preguntas a gran escala 

# Desventajas 

- No esta optimizado para hacer consultas a un registro en especifico 
- No esta optimizado para hacer la [[INSERT]] registro por registro
	- Por eso la escritura de los registros en un Data warehousing se hace mediante paquetes o [[bash]]

>[!WARNING] No todas las empresas necesitan DHW
>Puntos para identificar si necesitan un DHW
>- Múltiples fuentes de datos dispares
>- Requerimientos de análisis y visulizacion de big data en tiempo real
>- Necesidad de Ia y aprendizaje automatico
>- Analisis de straming
>- Generación de informes personalizados
>- [[Data mining]] y ciencia de datos

![[Pasted image 20240208083306.png]]