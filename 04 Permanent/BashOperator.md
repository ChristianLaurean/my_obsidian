---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
---


# Primer bashoperation

```python
from airflow import DAG
from datetime import datetime
from airflow.models import Variable
from airflow.operators.bash import BashOperator

pth = Variable.get("path")

  

with DAG(dag_id="Extract",

	description="Utilizando bash Operator",
	start_date=datetime(2024, 4, 4)) as dag:
	t1 = BashOperator(
	task_id="Download_file",
	bash_command=f"curl -o {pth}file.csv https://assets.datacamp.com/production/repositories/287/datasets/79b3c22c47a2f45a800c62cae39035ff2ea4e609/cars.csv"

)

t1

```
