---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
---


```python
from airflow import DAG
from datetime import datetime
from airflow.operators.python import PythonOperator

  

def decir_hola():
	print("HOLA!!!!!!!!!!")

  

with DAG(
		dag_id="Primer_dag_con_python",
		description="Es mi primer dag en python",
		schedule_interval="@once",
		start_date=datetime(2024,4,5)) as dag:

  

	t1 = PythonOperator(task_id="Python_task_1",
						python_callable=decir_hola)

	t1
```

