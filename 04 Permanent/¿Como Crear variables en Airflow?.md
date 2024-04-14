---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-images
---

# ¿Como Crear una Variable en Airflow?

1. Nos vamos al menú principal del webservices
2. `admin` y presionamos en variables
	1. ![[Pasted image 20240404115242.png]]

3. Podemos observar las variables que tengamos y crearlas
![[Pasted image 20240404115320.png]]

## Creando una variable
Es como un [[Diccionarios]] key, value
![[Pasted image 20240404120452.png]]
## ¿Como usarla en los [[¿Que es un DAG?]]?

![[Pasted image 20240404120553.png]]
O 
```Python
pth = Variable.get("path")
```
