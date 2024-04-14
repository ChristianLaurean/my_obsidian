---
Author: Platzi
Category: Linux
Type: Apunte
Status: Terminado
relación: "[[Terminal de Linux]]"
cssclasses:
  - page-white
---

# ¿Qué son las Wildcards?


Es una forma de hacer búsquedas mucho mas avanzadas usando patrones.

## Empezando a buscar archivos

```bash
ls *.py # muestranos todos los archivos que terminen en .py

ls datos* # muestranos todos los que empiecen con el nombre de datos 

ls datos? # muestrame todos los que empicen con el nombre y ? que tenga una coincidencia.

ls datos?? # lo mismo pero con dos concidencias

ls [[:upper:]]* # busca todo lo que tenga un carecter en mayuscula

ls [ad]* #que empiecen con ad
```