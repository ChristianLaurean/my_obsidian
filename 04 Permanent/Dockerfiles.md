---
Author: Coderhouse
Category: concepto
Type: Apunte
Status: Terminado
relación: "[[02 - Areas/DATA ENGINNER/Docker|Docker]]"
cssclasses:
  - center-images
  - center-titles
  - page-manila
  - pen-black
  - image-borders
---
Es un archivo de texto que no posee extensión. 
- Es como una receta para generar una [[imagen]] de [[04 Permanent/Docker|Docker]] 
- Es en donde se encuentran todos los comandos necesarios para crear una imagen y asi poder correr nuestra aplicación adentro de un contenedor..

![[Pasted image 20240315093918.png]]

---
## Comandos

### FROM
- Se usa para saber que sistema operativo o herramienta podemos usar como una imagen base.
	- `FROM ubuntu:21.21`
	- `FROM python:latest`
	- Las imagenes las encontramos en la pagina web.
### LABEL
- Son meta datos que estarán asociados a nuestra imagen.
	- Definimos las versiones
	- `LABEL version="1.0"`version de nuestr dockerfile
	-  `LABEL author="nombre"
### ENV
- Se usa para establecer variables de entorno mientras se crear la imagen de [[04 Permanent/Docker|Docker]]
	- `ENVIRONMENT_NAME=production`
	- `HOME=/opt/airflow` Estas se usan para el código o el sistema en si.
### EXPOSE
- Sirve mas para la documentación por ejemplo para que pueda ver que tipo de puertos debe de abrir para su correcto funcionamiento de la aplicación.
### RUN
- Sirve para ejecutar comandos en la terminal,ejecutar aplicaciones o paquetes que van a sumarse a la imagen. 
- ![[Pasted image 20240315102528.png]]
### COPY
- Nos permite copear archivos desde nuestro entorno de la maquina física hacia la imagen o contenedor de docker.
- ![[Pasted image 20240315102700.png]]
### WORKDIR
- nos permite cambiar el directorio base mientras estamos construyendo la imagen
- ![[Pasted image 20240315102943.png]]

### CMD
- Es como un RUN
- Este ejecuta comandos pero cuando se inicia el contenedor y es lo primero que se ejecuta cuando ya está el contenedor. 
- ![[Pasted image 20240315103114.png]]
