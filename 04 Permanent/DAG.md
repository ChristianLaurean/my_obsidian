---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-titles
---


# Declarando un DAG

![[Pasted image 20240404123412.png]]
![[Pasted image 20240404123446.png]]
```python
from airflow import DAG
from airflow.operators.empty import EmptyOperator
from datetime import datetime

with DAG(
	dag_id="id_unico",
	description="Descripción del DAG",
	start_date= datetime(2024,4,4)# Cuando empieza nuestro proceso
	schedule_interval="@once", # se ejecutara una vez
) as dag:

	t1 = EmptyOperator(task_id="nombre_unico de la tarea")
```

![[Pasted image 20240404123518.png]]
```python
from airflow.decorators import dag, task
from pendulum import datetime
import requests

@dag(
	 start_date=datetime(2024,02,01),
	 schedule="@daily",
	 tags=["pipeline"],
	 chatchup="False",
)

def tarea_dependencia():# EL nombre de la función de python es el id_task
	@task
	def get_activity():
		requests.get(url,timeout=10)
		return r.json()
	def archivo_crear(response):
		filepath = Variable.get("path")
		logica_para_crear
	response = get_activity()
	archivo_crear(response)
tarea_dependencia()
```

## Parámetros del DAG
- `start_date=datetime(2024,1,1)`: Es la fecha de inicio que el dag se programa
- `end_date=datetime(2024,05,01)`: Fecha Final
- `schedule="@daily`: Define la frecuencia con la que el programador activa  su dag [[Orquestación de Dags]]
- `tags=["Pipeline"]`: Son etiquetas para la interfaz
- `catchup=False` : Evita que se ejecute varias veces hasta llegar a la fecha de hoy.
- `default_args={"depends_on_past":True}: ` argumentos que tiene ariflow que podemos cambiar
- `max_active_runs=1` para que se ejecute un dag al dia

# 