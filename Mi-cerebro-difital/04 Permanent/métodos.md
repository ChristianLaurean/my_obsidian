---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Programación orientada a objetos]]"
---
### Métodos de instancia
Los métodos son como [[Funciones]]

```python
class Pajaro:
	def __init__(self.color):
		self.color = color
#Método son las acciones
# siempre poner self
	def piar(self):
		print(f"pio soy de color {self.color} ")
	def volar(self,metros):
		print(f"voló{metros}mts")
		self.piar()

piolin = Pajaro("rojo")
piolin.piar()# pio,soy de color rojo
piolin.Volar(12)#volo 12 mts

```
- Podemos modificar la instancia de clases
## Tipos de métodos

Usamos los [[Decoradores]] para poder usar estos metodos
###  Métodos de clase
 
```python
@classmethod
def mim_metodo(cls):#En vez de self usamo cls
	print("algo")
	cls.atributo_clase = True
```
- No podemos acceder a los atributos de instancia
- No necesitan de self para poder ejecutarse
- Si atributos de la clase
### Métodos estáticos

```python
class Mascota:
    
    @staticmethod
    def respirar():
        print("Inhalar... Exhalar")
        
mi_mascota = Mascota()
print(mi_mascota.respirar())
```
- No podemos acceder a los atributos de instancia ni de la clase
- Solo parámetros de entradas
