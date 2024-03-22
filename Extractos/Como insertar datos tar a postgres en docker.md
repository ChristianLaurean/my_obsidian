---
Author: Christian laurean
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Docker]]"
---
Primero debemos de enviar el archivo `.tar` al volumen.
```bash
docker cp ~/Descargas/dvdrental.tar my-db:/var/lib/postgresql/data
```

Después tenemos que ejecutar este comando que instala todas las tablas en postgres.

```bash
docker exec -i my-db pg_restore -U postgres -d dvdrental /var/lib/postgresql/data/dvdrental.tar
```


