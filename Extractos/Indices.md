---
Author: Coderhouse
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
Es un objeto de la base de datos, sirve para el acceso a la propia tabla y entonces lo primero que hace una base de datos es buscarlo por el indice y después por toda la tabla.
Es como un libro si buscas algo vas al indice primero y te tardas menos, pero si no usas el indice tienes que leer todo el libro.

# crear un indice

```sql
create index mi_indice on una_tabla(id, name);
```
