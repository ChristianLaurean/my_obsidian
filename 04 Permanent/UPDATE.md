---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# actualizar registros

```sql
UPDATE users
SET
	name_column = 'christopher'
	role = 'admin'
WHERE 'id' = 2;
```

# actualizar fechas

```sql
UPDATE calidad_aire
SET "Fecha_Hora_Medicion" = '2024-03-14 00:00:00.000'
WHERE id_calidad_aire = 1;
```