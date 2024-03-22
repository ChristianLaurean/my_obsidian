---
Author: Platzi
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
Los tipos de rango que vienen en [[PostgreSQL]] son:
- int4range: Que trae un rango de enteros. --> bool
- int8range: Es un rango de enteros grandes. --> bool
```SQL
select int4range(10,20) @>3; -- Si el 3 se encuentra dentro del rango entonces nos da un bool.
```
- numrange: Es un rango numérico.
```SQL
select numrange(11, 20) && numrange(12,30);
```
- tsrange: Es un rango del tipo timestamp pero sin la zona horaria.
- tstzrange: Es un rango del tipo timestamp con la zona horaria
- daterange: Es un rango del tipo fecha.  
    Esos son los que podemos usar como selectores de rango dentro de PostgreSQL si les interesa conocer más [Acá](https://www.postgresql.org/docs/9.2/rangetypes.html)

```SQL
SELECT UPPER(int8range(18,25)); -- nos trae cual es el numero mas grande (25)
```

```SQL
SELECT int4range(10,20) * int4range(15,25); -- retorna la intercepcion de los numeros
```

```SQL
SELECT ISEMPTY numrange(1,5);-- Esta vacio?
```

## ejemplo de uso
```SQL
SELECT *
FROM table
WHERE int4range(10,20) @> column;
```

```SQL
select int4range(min(tutor_id),max(tutor_id)) * int4range(min(carrera_id),max(carrera_id))
from platzi.alumnos;
```

# generando rangos

ES como un [[Range]]

```SQL
select *
from generate_series(1,5,2)
```

#### Generar rangos con fechas

```sql
select current_date + s.a as dates
from generate_series(0,14,7) as s(a);
```

![[Pasted image 20240129093940.png]]
