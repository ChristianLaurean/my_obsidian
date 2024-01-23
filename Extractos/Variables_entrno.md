---
Author: Christian laurean
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Entorno_antes_proyectos]]"
---
## Variables de entorno

### archivos
`touch .env` Local
`touch .env.dev` Desarrollo
`touch .env.pro`Produccion


En linux
```bash
export NAME_VARIABLE=value
echo NAME_VARIABLE
```

Exportar a python

```python
pip install python-dotenv


import os
from dotenv import load_dotenv
# Cargar las variables de entorno desde el archivo .env 
load_dotenv()
os.getenv("variable")

```

```python
import os
os.environ.get('NAME_VARIABLE')
```
