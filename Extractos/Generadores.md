---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---

Nos ayuda a generar o recorrer pero 1 en 1 en medida que lo estés necesitando para que no te lo de todo junto para no usar mas espacio en [[Ram]] 

Cuida la memoria de nuestra computadora

# Yield - Producir


```python
# En vez de usar retunr usaremos yield
def name_fun():
	yield da

g = name_fun()
print(next(g))# siguiente dato.

def name_fun():
	x = 1
	yield x
	x += 1
	yield x

g = name_fun()
print(next(g))# Tambien funciona asi.
```