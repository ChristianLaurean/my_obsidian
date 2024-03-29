---
Author: You Tube
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
`ìmport csv`


# Leer archivos csv

```python
with open('file') as file:
	archivo = csv.reader(file)#podemos iretarar
	for element in archivo:
		print(element)
```

# csv_diccionarios 

## leer csv 

```python
with open('file') as file:
	archivo = csv.DictReader(file)#podemos iretarar
	for element in archivo:
		print(element)
```

# escribir csv

```python
with open('file', mode='w') as file:
	columns = [columnas]
	archivo = csv.DictWriter(file,fieldnames=columns,delimiter=',')#listado de columnas
	archivo.writeheader()
	archivo.writerow(diccionario)#Escribe 1 por 1 en el archivo
	archivo.writerows(diccionario)# Tengo una lista de diccionarios
	
```
