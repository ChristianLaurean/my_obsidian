---
Author: DataCAMP
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-images
  - center-titles
---


## ¿Qué es el Airflow?


Airflow es una plataforma para crear, programar y supervisar  workflow.

- Creation
- Echeduling 
- seguimiento de workflows.


![[Pasted image 20240404092831.png]]

# Para que sirve airflow

Sirve para crear y gestionar Pipelines.

>[!warning]  Cuidado
>El propósito de ariflow es hacer la orquestación y no usar el computo
>Lo mejor es que todas las tareas se ejecuten en una maquina aparte por ejemplo en el ejemplo de SQL lo mejor es que el [[SELECT]] se ejecute en la base de datos.

## Ventajas y desventajas de usar airflow

>[!success] Ventajas
>- Manejo de dependencias: gran manejo de dependencias entre tareas asi permitiendo un flujo de datos.
>- Macros y Templantes: Está diseñado para operar en un cronograma basado en el tiempo, generalmente volviendo a ejecutar los mismo script con un rango de tiempo diferente.
>- Operadores: tiene muchos operadores que pueden usar para construir pipelines de manera sencilla
>- Ui y logs: tiene una excelente interfaz de usuario, donde puedes ver sus estados de los dags, verifica los tiempos de ejecución, verifixar los registros, volver a ejecutar tareas y mucho mas.
>- Es Open source la comunidad es muy activa


>[!danger] Desventajas
>- Procesamiento no tan intuitivo para principiantes
>- CI/CD es complicado: Si estas implmentando airflow en Docker, el proceso de CI/CD que reinicia el contenedor de Docker eliminara cualquier proceso de ejecución
>- No hay buen soporte en Windows: no es sencillo ejecucar airflow de forma nativa en windows. pero se mitiga con docker.


[[Data Pipelines]]
![[Pasted image 20240404094819.png]]
 
 Con Airflow se representa así:
![[Pasted image 20240404095118.png]]




