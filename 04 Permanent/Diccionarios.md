---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# ¿Qué Son los Diccionarios?

>[!tip] Es un objeto que se organiza por Clave:Valor
>```python
>my_dict = {"nombre":"chris", "Apellido":"Laurean"}
>
># No tiene index
>#Solo se buscan valores por sus Claves
># Puede tener todos los tipos de datos, hazta listas,diccionarios ETC.
>```

## CRUD
```python
# acceder al diccionario
mi_dict["nombre"]
# Lo podemos guardar en una variable
variable = mi_dict["nombre"]
#Agregar un nuevo elemento
mi_dict["key"] = "Valor"
#actualizar
mi_dict["nombre"] = "nuevo_valor"
#Eliminar
del mi_dict
```

## Métodos

```python
#Extrae todas las llaves
mi_dict.keys()#Retorna una tupla con todas las llaves

# Extraer todos los valores
mi_dict.values()#Retorna una tupla con todos los valores

# Extrae todo keys y valores
mi_dict.items()#Retorna una tupla con todos los valores y keys
```

