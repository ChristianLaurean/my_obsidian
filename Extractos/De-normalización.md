---
Author: Coderhouse
Category: Bases de datos
Type: Apunte
Status: Terminado
relación: "[[INGENIERÍA DE DATOS]]"
---
# Que es la de-normalización?

- Es hacer todo a la inversa de lo que hacíamos en [[Normalización]] para mejorar el [[Performance]]
- Las usamos mas en [[OLAP]]
- Usamos pocas tablas que combinen datos de otras tablas 
- Consumimos mas [[Almacenamiento]] pero esto no es costoso.

>[!danger] Evitar
>- Evitar actualizar datos que tengan [[Redundancia]]


>[!succes] Soluciones
>- Evitamos el uso de [[Joins]] Excesivos por que ya no están tan divididas las tablas y eso favorece el rendimiento de la consulta
>- Tenemos la información mas rápida 

