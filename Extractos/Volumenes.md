---
Author: Platzi
Category: concepto
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Docker|Docker]]"
---
Son espacios compartidos de nuestra computadora física y el [[Contenedor]].
- sirven para agregar grandes cantidades de datos
```bash
docker run -it --rm -d -p 8080:80 -v ./nombre_carpeta:capeta_volumenes --name nombre id_img

```

En [[Dockerfiles]]
![[Pasted image 20240316101856.png]]