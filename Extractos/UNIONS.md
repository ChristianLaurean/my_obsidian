---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---

# UNION


>[!tip] ¿Para que sirve?
>`UNION` Toma dos tablas como entrada y devuelve todos los registros de ambas tablas pero apila los datos entre filas
>![[Pasted image 20231205112243.png|100]]
**Si los registros son idénticos, `UNION` los devuelve una vez**
![[Pasted image 20231205111352.png|500]]

>[!WARNING] PODEMOS UNIR CUALQUIER COSA, HASTA CONSULTAS DIFERENTES DE LA MISMA TABLA
>```SQL
>select code,name from public.continent where name in ('Asia','Europe')
union
select code,name from public.continent where name LIKE '%America%';
>```


### Código

>[!example] `UNION`
>```SQL
>SELECT *
>FROM left_table
>UNION
>SELECT *
>FROM right_table;
>```

## UNION ALL

>[!tip] ¿Para que sirve?
Este lo que hace es hacer lo mismo que `UNION` solo que también pondrá valores duplicados.
![[Pasted image 20231205111518.png|500]]

### Código

>[!example] `UNION ALL`
>```SQL
>SELECT *
>FROM left_table
>UNION ALL
>SELECT *
>FROM right_table;
>```


# INTERSECT

>[!tip] ¿Para que sirve?
>`INTERSECT` Toma dos tablas como entrada y devuelve todos los registros que están relacionadas de ambas tablas
>![[Pasted image 20231205112848.png|100]]
>![[Pasted image 20231205113046.png]]

### Código

>[!example] `UNION ALL`
>```SQL
>SELECT *
>FROM left_table
>INTERSECT
>SELECT *
>FROM right_table;
>```

>[!WARNING] La diferencia con las INNER JOINS
> - INNER JOINS devuelve datos duplicados y INTERSECT NO

# EXCEPT

>[!tip] ¿Para que sirve?
>`EXCEPT` Nos permite identificar que registros están presentes en una tabla pero no en la otra.
>![[Pasted image 20231205115310.png|100]]
>![[Pasted image 20231205115414.png]]

 ### Código

>[!example] `UNION ALL`
>```SQL
>SELECT *
>FROM left_table
>EXCEPT
>SELECT *
>FROM right_table;
>```

