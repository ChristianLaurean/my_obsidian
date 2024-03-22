---
Author: Coderhouse
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Docker|Docker]]"
---
Es una unidad de [[Software]] que contiene todo lo necesario para correr una aplicación o un servicio.

- Estandarización 
	- Nos permite portabildiad bajo cualquier entorno.
- Ligeros
	- Por que los contenedores que virtualizan por completo todo el S.O si no que solo hace uso de su [[karnel]]
- Seguros
	- Contiene un entorno de aislamiento que permite que una aplicación solo haga uso de todo lo que esta adentro de ese contenedor. 

```docker
docker run ID o nombre_img
docker run -it --rm -d -p 8080:80 --name nombre id_img
```


Para hacer el contenedor tenemos los prametros:
`-it` : interativo para ver la logs
`-rm` : es para eliminar cualquier version del contenedor
`-d`:  Es para que se ejecute en segundo plano
`-p`: Son los puertos es la puerta de entrada a mi app. Es como un tunel entre un puerto al que yo me comunico con docker y otro en donde docker se comunica con la app.
`--name`: nombre del contenedor

# Administrar mis contenedores de Docke
- `Docker ps --size`: ver el tamaño que esta usando el contenedor
- `Docker stop ID_contenedor` : Parar un contenedor.
 



























