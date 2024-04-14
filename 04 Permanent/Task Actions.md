---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-titles
  - center-images
---


# Estados de una Tarea
![[Pasted image 20240406112932.png]]

## **Los estados posibles para una instancia de tarea son:**

none: la tarea aún no se ha puesto en cola para su ejecución (todavía no se cumplen sus dependencias)

scheduled: el programador ha determinado que se cumplen las dependencias de la tarea y debería ejecutarse

queued: La tarea ha sido asignada a un Ejecutor y está esperando un trabajador

running: La tarea se ejecuta en un trabajador (o en un ejecutor local/síncrono)

success: La tarea terminó de ejecutarse sin errores

shutdown: Se solicitó externamente que la tarea se cerrara cuando se estaba ejecutando

restarting: Se solicitó externamente que la tarea se reiniciara cuando se estaba ejecutando

failed: La tarea tuvo un error durante la ejecución y no pudo ejecutarse

skipped: La tarea se omitió debido a bifurcación, LatestOnly o similar.

upstream_failed: una tarea ascendente falló y la regla de activación dice que la necesitábamos

up_for_retry: La tarea falló, pero quedan reintentos y se reprogramará.

up_for_reschedule: La tarea es un Sensor que está en reschedulemodo

deferred: La tarea se ha aplazado a un activador

removed: La tarea ha desaparecido del DAG desde que comenzó la ejecució


# Task action

### Estados del clear
![[Pasted image 20240406113734.png]]
- Past: Lo que hace es volver a ejecutar el ciclo de las tareas del pasado(Horizontal)
- Future: ejecuta las tareas del futuro(Horizontal)
- Upstream: Limpiezas ya con dependencias anteriores o dependencias padres.(Vertical)
- Downstream: Limpieza de las tareas depues. (Vertical)
- si no selecionas nada solo se ejecuta el primer.

## MARK FAILED
Marcar un proceso a proposito un fallo.