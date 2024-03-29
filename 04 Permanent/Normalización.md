---
Author: Coderhouse
Category: Modelado de datos
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Diseño de bases de datos|Diseño de bases de datos]]"
---
# ¿Qué es la normalización?

Son una serie de pasos o de reglas que se deben de  seguir para crear bases de datos funcionales

## Objetivo

- Evitar la [[Redundancia]]
- Evitar la inconsistencia de los datos 
- Hacer una bases de datos mas optimizada para las transacciones [[OLTP]]
# 1FN

>[!tip] COMPROBACIÓN Y 0 CLONACIÓN
>1. Comprobar que cada celda debe de tener 1 solo dato único
>2. 0 clonación: separar los [[Atributos]] que no sean de la misma tabla
>3. Que todas tengan su [[Primary key]]
>4. No debe de  tener datos duplicados!!
>Ejemplo
>![[Pasted image 20240201084031.png]]
>Ya normalizada
>![[Pasted image 20240201084130.png]]


# 2FN

>[!tip] DIVIDE Y VENCERAS
>1. debe cumplirse la **1FN**
>2. Todas las columnas de la tabla deben de pertenecer a una [[Keys - Llaves|Primary key]] **Completa**(si hay [[Clave compuesta]]) o solo [[Primary key]]
>3. No deben de tener una [[Dependencias Parciales]]
>4. Dividimos las tablas que no dependan de la llave primaria
>![[Pasted image 20240201085531.png]]
>Normallizada
>![[Pasted image 20240201091005.png]]
>


# 3FN

>[!tip] El IMPOSTOR
>1. Debe de cumplir la **1FN** y **2FN**
>2. encontrar el impostor con [[Dependencias Transitivas]] si hay [[Dependencias Transitivas]] y no una [[Dependencias funcionales]] la separamos a otra tabla.
>![[Pasted image 20240201091210.png]]
>Normalización
>- dividimos para que tengan cada tabla [[Dependencias funcionales]]
>![[Pasted image 20240201091243.png]]
>![[Pasted image 20240201091311.png]]
>- Como tiene una [[Relaciones|relación]] Muchos a muchos creamos una Tabla Transitiva para romper ese muchos a muchos.
>![[Pasted image 20240201091817.png]]


