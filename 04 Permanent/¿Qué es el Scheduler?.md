---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-images
  - center-titles
---


# # Scheduler

1. **Scheduler**: El Scheduler es el corazón de Airflow. Su tarea principal es determinar cuándo ejecutar cada tarea en un DAG. Regularmente examina la carpeta de DAGs en busca de cambios o nuevas definiciones de DAGs. Cuando detecta cambios, planifica la ejecución de las tareas basándose en la programación definida en el DAG y en las dependencias entre tareas.
    
2. **Executor(El jefe)**: El Executor es responsable de ejecutar las tareas programadas por el Scheduler.
	- Airflow admite varios tipos de Executors: 

		- Airflow LocalExecutor: las tareas se ejecutan en los Workers dentro del mismo sistema donde se ejecuta Airflow

		- Airflow CeleryExecutor:Nos permite dividir la carga de trabajo en diferentes [[Workers]] y cada uno ejecutarse en una maquina diferente.

		- Airflow Kubernetes
	Executor que determinan cómo y dónde se ejecutan las tareas. 
    
3. **Workers**(Trabajadores): Los Workers son procesos que ejecutan las tareas en nombre del Executor. Reciben las tareas de la cola de tareas las ejecutan en el entorno configurado. 
    
4. **Metadata Database**: Airflow utiliza una base de datos para almacenar metadatos relacionados con los DAGs, las tareas y las ejecuciones.
    
5. **Web Server**: El Web Server proporciona una interfaz web para interactuar con Airflow. 

![[Pasted image 20240404110453.png]]

# Ejecutores
Airflow Celery Executor



1. Scheduler es el que manda las novedades y estas novedades llegan al execute(Airflow Celery Executor).
	1. Distribulle la tarea a diferentes [[Workers]]
	2. Si la tarea falla entonces lo que hace es darle la tarea a otro worker que no este fallando y este libre.
