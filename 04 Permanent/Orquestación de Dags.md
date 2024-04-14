---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Proceso
relación: "[[Airflow]]"
cssclasses:
  - page-white
---
`preset` : son maneras ya predeterminadas que tiene airflow para ver cuando se ejecutaran nuestros procesos o [[DAG]]

![[Pasted image 20240406103354.png]]
`None`: No quiero que se ejecute hasta que otro DAG lo llame.
`@once` Se ejecuta solo una vez
`hourly` Ejecutate cada hora

Si prefieres ser mas especifico podemos usar la sintaxis de [[CRONTAB]]
