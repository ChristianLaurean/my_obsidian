---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
# Pickled

Es un tipo de archivo nativo de [[Python]] y es un archivo donde podemos almacenar listas y diccionarios. 

`rb` = modo archivo binario

```python
import pickle

with open(file,'rb') as file:
	 data = pickle.load(file)
```
