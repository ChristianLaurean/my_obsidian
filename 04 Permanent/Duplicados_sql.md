---
Author: Platzi
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# Encontrar duplicados

- Rara vez encontramos duplicados por el **id**
1 de las formas
```SQL
select
	(a.nombre,
	a.apellido,
	a.email,
	a.colegiatura,
	a.fecha_incorporacion,
	a.carrera_id,
	a.tutor_id)::text,
	count(*)
from platzi.alumnos as a
group by 1
having count(*) > 1 ;
```

Con [[WINDOW FUNCTIONS]]

```SQL
select *
from (
	select 
		id,
		row_number() over(
		partition by
		nombre,
		apellido,
		email,
		colegiatura,
		fecha_incorporacion,
		carrera_id,
		tutor_id
	order by id
	) as row_id,
	*
	from platzi.alumnos
) as duplicados
where row_id > 1;
```
# Eliminar duplicados
