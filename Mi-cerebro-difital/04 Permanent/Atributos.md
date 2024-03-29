---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Programación orientada a objetos]]"
---
Esto es igual a los atributos en las [[Base de datos]] y programación

# Atributos en python
## Atributos de clase

Son atributos que pertenecen a la [[CLASE]] y serán para todos los objetos que creamos para esa misma clase.

## Atributos de instancia

Son atributos que pertenecen a la instancia o al [[objetos]] y estos pueden variar dependiendo del objeto.

```python
class Pajaro:
	# Atributos de clase
	alas = True


	# Método constructor: Es lo primero que ve nuestra clase para ver que atributos necesita para que el objeto pueda ejecutarse correctamente   
	def __init__(self, color,especie):# self significa el mismo y es la instancia del objeto que se va a crear 
		self.color = color # asigna los atributos a el pajaro
		#atributo de instancia
		self.especie = especie


cotorro = Pajaro("rojo","Cotorro")
print(cotorro.color)
print(cotorro.especie)
```
