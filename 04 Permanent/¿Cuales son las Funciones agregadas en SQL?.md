---
Author: Udemy
Category: SQL
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
cssclasses:
  - center-images
  - center-titles
  - page-white
---
## Funciones Agregadas

>[!tip] sirven
Nos sirven para resumir valores y agrupar valores con [[GROUP BY]]

### Numéricos


>[!example] Codigo completo [[1 - SQL|SQL]]
>- `AVG` Promedio
>- `ROUND(numeroa redondear, decimales que queremos redondear)` sirve para redondear números decimales
>```SQL
>SELECT ROUND(AVG(Gastos), 2)
>FROM empleos
>WHERE year > 2000
>```
>Es una buena forma para resumir el promedio
>`SUM` Suma
>```SQL
SELECT sum(names) AS suma_names
FROM empleos;
>```

### **No numéricos**

`MIN` Maximo
`MAX` Minimo
## Count

>[!example] Codigo completo [[1 - SQL|SQL]]
>`COUNT` nos devuelve un numero del conteo de todas las filas 
>**Esto se puede realizar con los campos que quieras.**
>```SQL
SELECT COUNT(names), COUNT(fechas)
FROM empleos;
>```
>Contamos los valores unicos de la columna
>```SQL
>SELECT COUNT(DISTINCT nombre_tabla)
>FROM empleos;
>```

