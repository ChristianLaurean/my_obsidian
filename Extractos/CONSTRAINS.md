---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
>[!tip]
>Son restricciones que le ponemos a la base de datos con el objetivo de que evitemos la basura

# Check

>[!tip] Constraint especial
>Es 1 o mas verificaciones que queramos hacer sobre un campo o varios.
>```SQL
>ALTER TABLE country ADD  CHECK(
>	columna >= 0
>	);
>	
>```
>Funciona como un [[WHERE]] por que podemos usar un filtrado que nosotros queramos.
>```SQL
>ALTER TABLE country ADD  CHECK(
>	columna in ('pais','otro_pais')
>	);
>	
>```


# [[Keys - Llaves|Foreign Keys]]

```sql
ALTER TABLE name_table
	add CONSTRAINT fk_name_foreignkey
	FOREIGN KEY (nombre_columna)
	REFERENCES nombre_otra_table(id);
```

>[!warning] Actualización en cascada
>`ON UPDATE CASCADE`
>`ON DELETE CASCADE` --> CUANDO QUIERO QUE SE ELIMINE UN REGISTRO O ACTUALIZAR SE HAGA EN CASCADA OSEA EN LAS DOS TABLAS.




