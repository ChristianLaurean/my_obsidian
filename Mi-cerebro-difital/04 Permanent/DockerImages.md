---
Author: Coderhouse
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Docker|Docker]]"
---
Es un archivo con intrucciones para generar un contenedor de Docker.

- Son un punto de partida para crear otras imágenes
- También sirven para tener un punto de restauración

```bash
docker build -t nombre_docker:versión ubicacióndockerfile #generamos la imagen
```

****
# Administrar mis imágenes de Docker

**Buscar imágenes**
- `docker images nombre_imagen`
- `docker images --filter=referece='*:1.0'` Traeme todas las imágenes que el tag sea 1.0
- `docker images tag sitioweb:latest amin/sitioweb:latest`: creo una nueva imagen usando otra imagen
**Eliminar imagenes y etiquetas**
`docker rmi ID o nombre`
`docker rmi -f ID o nombre` forzar la eliminación.
`docker stop id_img`
