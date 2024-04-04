---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - center-titles
  - center-images
  - page-white
---


# Es importante que el data Pipeline sea:


Resiliencia: El pipeline debe ser capaz de manejar fallas y errores de manera efectiva, asegurando que pueda recuperarse de manera adecuada sin comprometer la integridad de los datos.

Idempotencia: Es fundamental que el pipeline produzca el mismo resultado cada vez que se ejecute, sin generar duplicados ni resultados inconsistentes, incluso si se ejecuta varias veces.

Escalabilidad: El diseño del pipeline debe ser capaz de manejar grandes volúmenes de datos y una mayor frecuencia de ejecución a medida que crece la demanda, garantizando un rendimiento óptimo en cualquier situación.

Transparencia: Se debe evitar el uso de operaciones opacas o "cajas negras" en el flujo de datos. Todos los procesos deben estar bien probados, documentados y comprensibles para todos los involucrados en el proyecto.>)

	

>[!warning] Antes de pasarla a producción
	>- Hacer pruebas unitarias
	>- debe probarse de un extremo a otro, utilizando pequeños como grandes archivos vacios o incluso datos incorrectos.
	>- El codigo debe de ser revisado antes de procución con [[Logging]]
