---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
>[!tip] conceptos
>E/S = Entrada / Salida
>I/O= Input / Output

##### modos de apertura:
- r: lectura
- w: escritura y sobrescrita. Se crea si no existe
- a: escritura pero se posiciona hasta al ultimo del archivo. se crea si no existe
## Abrir un archivo

```python
with open('path',mode='r') AS file:
	file.read()#Lee todo el archivo
	file.readline()#Es un iterador y solo lee la primera linea pero si lo pones varias veces se va ejecutando uno por uno.
	file.readlines()#se mete todo a una lista pero es peligroso por que sobrecarga la memoria.
	for linea in file:
		print(linea)
```

## Crear y escribir archivos
```python
with open(path, mode='w') as file:
	file.write('texto')
	file.writelines(['hola','mundo'])
```