---
Author: You Tube
Category: Programación
Type: Video
Status: Terminado
relación: "[[Curso de Python]]"
---
# trabajar con fechas

```python
from datetime import datetime

# fecha_hora actual
fecha_actual = datetime.now()

# fecha que le demos al contructor
fecha = datetime(2024,5,3)
# Tambien le puedes dar minutos y segundos

# formato personalizado
fecha_perso = datetime.strftime(fecha, '%d/%m/%Y %H:%M:%S')

fecha_perso = datetime.strftime(fecha, '%b/%d/%Y %H:%M:%S') # %b es mes abreviado B

# https://www.programiz.com/python-programming/datetime/strftime

# de str a datetime 

fecha_perso = datetime.strptime(fecha, '%d/%m/%Y %H:%M:%S')
```