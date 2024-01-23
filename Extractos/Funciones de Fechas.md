---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# Manejo de fechas

## Nos da la fecha de ahora.

Esta nos da la fecha actual con hora, minutos y segundo

```SQL
SELECT CURRENT_DATE; -- Solo fecha
SELECT NOW;-- Fecha, hora 
SELECT CURRENT_TIME; -- Solo hora



select date_part('minutes', columna_que tenga date o time) -- Extraemos una parte de la fecha
select date_part('days'columns)
select date_part('months'columns)
select date_part('years'columns)
select date_part('hours'columns)
```

### Consultas con fechas

```SQL
select * 
from employees
where hire_date BETWEEN '1998-02-05' AND '2000-01-01'
order by hire_date desc;
```


```SQL
select max(hire_date) as nuevo 
from employees;
```


## intervalos

```SQL
hire_date + INTERVAL '1 day'
hire_date + INTERVAL '1 month'
hire_date + INTERVAL '1 year'
-- Año y mes
hire_date + INTERVAL '1.1 year'
-- año + mes y año.
hire_date + INTERVAL '1.1 year' + INTERVAL '1 day'

-- Forma dinamica de sumar una fecha
select
	max(hire_date) + make_interval(years:=23)
from employees e ;


select
make_interval(years := 2024 - extract(YEARS from hire_date)::integer),

make_interval(years := date_part('years',current_date)::integer - date_part('year',hire_date)::integer) as opcion2

from employees e ;


```

