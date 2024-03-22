---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
# HDF5

Es un archivo que nos ayuda almacenar grandes cantidades de datos numericos.


```python 
import h5py

filename = file
data = h5py.File(filename,'r)
print(data)
```

--- 
Manipulación como un [[Diccionarios]]

```python
for i in data.keys():
	print(i)#Documentos o grupos del archivo
# meta: Metadatos del archivo
# quality: información sobre la clidad de los datos
# strain : contiene medidas 

