---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
```sql
SELECT 
CASE --if              que muestro
	when columa > algo then 'Rango a'
	-- Podemos poner todos los when que sea necesario
	--Se puede dejar asi
	-- Pero mejor:
	else 'Rango D'
END AS rango

FROM table_a
```

![[Pasted image 20240125110819.png]]

# CASE EN [[¿Como Usar WHERE?]]

Asi podemos filtrar con Case 
En este caso solo usamos los null
```SQL
select
	b.producto,
	a.venta_total_$,
	c.nombre || ' ' || c.apellido as nombre ,
	case
		when a.venta_total_$ > 600 then 'cumplido'
		when a.tienda = 1 then 'sin metric'
	end as meta
from practica.ventas as a
inner join practica.productos as b on a.producto = b.id_prod
inner join practica.vendedores as c on a.vendedor = c.id_vend
where case
		when a.venta_total_$ > 600 then 'cumplido'
		when a.tienda = 1 then 'sin metric'
		end is NULL
order by a.venta_total_$;
```