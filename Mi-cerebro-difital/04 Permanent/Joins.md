---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---

# UNIONES

>[!tip] ¿Qué son?
>Con las uniones podemos unir tablas gracias a una referencia de otra tabla por ejemplo las [[2 - Primary Key|Primary Key]] o otro campo de la tabla.
>![[Pasted image 20231205075801.png|300]]

# INNER JOIN

>[!tip] Para que sirve
>Lo que hace es buscar solo los registros que tengan ambas tablas con los mismos valores
>![[Pasted image 20231205080034.png|300]]
>**Resultado**
>![[Pasted image 20231205080105.png|300]]

### Código

>[!example] inner join
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 INNER JOIN table_derecha
>3 ON tabla_izquierda.colum_reference = tabla_derecha.colum_reference;
>```
> **Podemos usar AS Para facilitar la lectura**

Se utiliza `USING` cuando el campos que se van a unir tenga el nombre idéntico 

>[!example] inner join + using
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 INNER JOIN table_derecha
>3 USING(colum_con_name_identico)
>```
>Hace que el código sea mas corto

---
# LEFT JOINS

>[!tip] Left joins
>Es una unión que te devolvera todos los resultados de la tabla izquieda y aquellos que se relacionan con la tabla derecha.
>![[Pasted image 20231205100100.png]]

## Código

>[!example] LEFT JOIN
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 LEFT JOIN table_derecha
>3 ON tabla_izquierda.colum_reference = tabla_derecha.colum_reference;
>```
> **Podemos usar AS Para facilitar la lectura**
 
---

# RIGHT JOIN

>[!tip] RIGHT JOIN
>Es lo mismo que el LEFT JOIN solo que agarraremos todos los datos de la tabla derecha y los datos que hacen match con la tabla izquieda.
>![[Pasted image 20231205100654.png]]

## Código

>[!example] RGHT JOIN
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 RIGHT JOIN table_derecha
>3 ON tabla_izquierda.colum_reference = tabla_derecha.colum_reference;
>```
> **Podemos usar AS Para facilitar la lectura**

---
# FULL JOINS

>[!tip] ¿Cómo funciona?
>Es la función de LEFT JOIN Y RIGHT JOIN 
>Devuelve todos los registros de las dos tablas, no importa si no tienen relación o no.
>![[Pasted image 20231205101337.png]]

## Código

>[!example] FULL OUTER JOIN
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 FULL JOIN table_derecha
>3 ON tabla_izquierda.colum_reference = tabla_derecha.colum_reference;
>```
> **Podemos usar AS Para facilitar la lectura**

---

# CROSS JOIN
>[!tip] ¿Qué son?
>Uniones cruzadas
>busca todas las combinaciones posibles que tengan una relación con la otra tabla
>![[Pasted image 20231205102203.png|500]]

## Código
>[!example] CROSS JOIN
>```SQL
>4 SELECT *
>1 FROM table_izquierda
>2 CROSS JOIN table_derecha;
>```

---
# SELF JOIN

>[!tip] ¿Qué son?
>Cuando una tabla se une consigo misma
>Se usan para comparar valores de parte de una tabla con otros valores dentro de la misma tabla


## Código

>[!example] SELF JOIN
>```SQL
>select pm.country, pm2.country, pm.continent
>from prime_ministers AS pm
>inner join prime_ministers  AS pm2
>on pm.continent = pm2.continent;
>```

---
# Múltiples JOINS


>[!example] inner join 
>```SQL
>6 SELECT *
>1 FROM table_izquierda AS tz
>2 INNER JOIN table_derecha AS td
>3 ON tz.colum = td.column
>4 INNER JOIN otra_table AS ot
>5 ON table_iz_or der.colum = ot.colum;
>```
>Puede ser cualquier tabla con la que lo relacionamos

Hay veces que hay errores y pasan datos duplicados lo que podemos hacer para limitar los registros es usar `AND`

>[!example] inner join + `AND`
>```SQL
>5 SELECT *
>1 FROM table_izquierda AS tz
>2 INNER JOIN table_derecha AS td
>3 ON tz.colum = td.column
>4      AND tz.otra_colum = td.otra_colum 
>```
>![[Pasted image 20231205090318.png]]



