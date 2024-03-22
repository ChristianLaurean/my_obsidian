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
# debug = 10
# info = 20
# Warning = 30
# Error = 40
# Criitical = 50

logging.BasicConfig(level=20
				   format="%(process)s - %(levelname)s - %(asctimes)s") - Message:%(message)s",
				   datefmt="%Y-%m-%d"
logging.debug('hay')
import logging

logging.basicConfig(level=logging.DEBUG, format="%(levelname)s - %(asctime)s - Message: %(message)s", datefmt="%Y-%m-%d")

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