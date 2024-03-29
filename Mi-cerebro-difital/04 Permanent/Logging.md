---
Author: codigofacilito
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
```python
import logging

# Nivel de prioridad
# debug = 10: proporcionan datos como la dimensionalidad de los datos, el tipo y los valores de las variables
# info = 20: notifica las operaciones que ocurren en los datos
# Warning = 30: ocurre cuando pasa algo inesperado pero no a ocurrido un excepción, numero inesperado de filas o tipos de datno no vistos.
# Error = 40 cuando ocurre una excepción que deberia de detener la ejecución
# Criitical = 50

logging.BasicConfig(level=20
				   format="%(process)s - %(levelname)s - %(asctimes)s") - Message:%(message)s",
				   datefmt="%Y-%m-%d"
logging.debug('hay')
import logging

logging.basicConfig(level=logging.DEBUG, format="%(levelname)s - %(asctime)s - Message: %(message)s", datefmt="%Y-%m-%d")

```

```python
# Create an info log regarding transformation

logging.info("Transformed 'Order Date' column to type 'datetime'.")

# Log the dimension of the DataFrame before and after filtering

logging.debug(f"Shape of the DataFrame before filtering: {raw_data.shape}")

logging.debug(f"Shape of DataFrame after filtering: {clean_data.shape}")
```
# archivos logs

```Python
import logging

logging.BasicConfig(level=20
				   format="%(process)s - %(levelname)s - %(asctime)s") - Message:%(message)s",
				   datefmt="%Y-%m-%d",
				   filename="nombre_archivo.log",
				   filemode="a"
```
