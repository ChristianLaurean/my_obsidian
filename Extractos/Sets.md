---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# ¿Qué son los Sets?

>[!tip] Es un tipo de dato
>Es una colección de elementos igual que las [[listas]]
>```python
>Se declaran de dos maneras
>set([1,2,4])
>mi_set = {1,2,3,4,5}
>```
>- Solo admiten elementos únicos
>- No están ordenados por indice
>- Son inmutables
>- No listas y [[Diccionarios]]

## Metodos

```python
# Se unene
mi_set = {1,2,3}
mi_set2 = {3,4,5}
mi_set3 = mi_set.union(mi_set2)

# Agregar
mi_set.add(4)

# eliminar
mi_set.remove(3)
mi_set.discard(3)# si no existe,no me da error
mi_set.pop()#Elimina el ultimo o el que quieras
mi_set.clear()#Elimina todo
```
