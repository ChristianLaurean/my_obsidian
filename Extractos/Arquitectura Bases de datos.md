---
Author: Coderhouse
Category: Fundamentos de Data
Type: Apunte
Status: Terminado
relación: "[[Fundamentos de Bases de datos]]"
---
La arquitectura de datos se centra en el diseño,desarrollo,mantenimiento de programas informáticos que almacenan y organizan información .

La arquitectura depende de cuantos usuarios están conectados a la base de datos y cuales son las necesidades de cada uno.

# tipos de arquitecturas

- **Tier 1**
	- Es cuando la [[Base de datos]] Puede ser usada por los usuarios y cualquier cambio puede tener efecto en la [[Base de datos]]
	- Se requiere una respuesta rápida 
	- Ejemplo: Se usan para el desarrollo de aplicaciones locales para la empresa.
	- ![[Pasted image 20240118092421.png]]
- Tier 2
	- El cliente se comunica con la [[Base de datos]] por medio de aplicaciones, [[Curso de APis|Apis]], conectores ODBC y JDBC
	- Esto se usa cuando el cliente y la [[Base de datos]] no se encuentra en la misma maquina y se usa un servidor para conectarnos a ella.
	- ![[Pasted image 20240118093220.png]]
- Tier 3
	- El cliente no puede comunicarse directamente con la base de datos,tiene dos [[Servidor|servidores]] uno es la **capa lógica** y el otro es la capa de [[Datos]] lo cual garantiza integridad.
	- Se usa para aplicaciones webs de gran escala. 
	- ![[Pasted image 20240118094112.png]]
- Tier 4
	- Multilayer
	- Tiene distintas capas o layers están separadas para manejar las funciones para el procesamiento, gestión de datos y presentación  de forma independiente y nos brinda una gran seguridad y flexibilidad
	- Tiene 3 componentes: Web Server, web Conteiner y Application Server
	- ![[Pasted image 20240118094346.png]]

# Componentes principales de la arquitectura de [[Base de datos]]

1. Hardware: Es la parte física que permiten el [[Almacenamiento]]
2. [[Software]]: refiere al conjunto de programas para manejar y controlar los datos osae los [[DBMS]] y [[redes]]
3. [[Datos]]
4. [[Procedimientos]] : Son las instrucciones utilizadas en un [[DBMS]] y es configurar, iniciar y cerrar sesiones, administrar operaciones diarias, Realizar copias de seguridad de los datos
5. Lenguaje de acceso a las bases de datos osea [[SQL]]

## Modos para dar Acceso
- Centralizado
	- Toda la información se aloja en una sola ubicación y para acceder a ella se utiliza Internet. LAN,WLAN o otras
	- ![[Pasted image 20240118110753.png]]
	- 
- Desentralizado
	- Se almacena la información en una red de computadoras distribuidas en lugar de un único servidor centralizado
	- ![[Pasted image 20240118110814.png]]