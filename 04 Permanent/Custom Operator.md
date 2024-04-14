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


# Como crear un CustomOperator

1. Crear un archivo
2. importamos la libreria
	1. `from airflow.models.baseoperator import BaseOperator` creamos nuestros operadores

>[!success] Importante
>El BaseOperator va heredar la clase que hagamos
>```python
>class Nombre(BaseOperator)
>	def __init__(self,name, **kwargs):
>		super().__init__(**kwargs)
>			self.name = name
>	def execute(self,context):
>		print(self.name)
>```

# en el archivo DAG
Solo importamos el nombre del archivo y nombre de la clase.
`from nombre_archivo import nombre_class`
