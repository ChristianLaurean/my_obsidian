---
Author: Coderhouse
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
---

# Variables de Context

Son estructuras que nos sirven para pasar información.
`*context` Variables numericas
`**context` strings

`provide_context=True` con esto definimos que estamos pasando la información de las tareas para todos los operadores

>[!success] Beneficiós
>- Nos permiten monitorear la ejecución de los operadores
>- Mecanismos como variables de entorno

## ds
Representan la fecha

## ts
y hora de ejecución de una tarea

![[Pasted image 20240406121935.png]]