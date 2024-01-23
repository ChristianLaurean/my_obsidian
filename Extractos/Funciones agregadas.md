---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
## Funciones Agregadas
>[!tip] sirven
Nos sirven para resumir valores y agrupar valores con [[GROUP BY]]

- Numéricos
`AVG` Promedio
`ROUND(numeroa redondear, decimales que queremos redondear)` sirve para redondear números decimales

>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
>SELECT ROUND(AVG(Gastos), 2)
>FROM empleos
>WHERE year > 2000
>```
>Es una buena forma para resumir el promedio

`SUM` Suma

- **No numéricos**

`MIN` Maximo
`MAX` Minimo
`COUNT` nos devuelve un numero del conteo de todas las filas 

**Esto se puede realizar con los campos que quieras.**
>[!example] Codigo completo [[1 - SQL|SQL]]
>```SQL
SELECT COUNT(names), COUNT(fechas)
FROM empleos;
