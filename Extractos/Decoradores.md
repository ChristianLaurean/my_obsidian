---
Author: Udemy
Category: Programación
Type: Video
Status: Terminado
relación: "[[Curso de Python]]"
---
```python
def decorar(funcion)
	def otrafuncion(palabra):
		print("hola")
		funcion(palabra)#Es como si fuera: mayuscula(texto)
		print("adios)
		
@decorar		
def mayuscula(texto):
	print(texto.upper())
	
def minusculas(texto):
	print(texto.lower())

```