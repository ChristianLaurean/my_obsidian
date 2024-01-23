---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# ¿Qué son las listas?

>[!tip] Es una secuencia ordenada de objetos
>```python
>mi_lista = [10,"hola",True,5.2]
>lista_anidada = [[10],[12]]
># Concatenar Listas
>mi_lista + mi_lista2 # se concatenan
>```

## CRUD con listas

```python
#Agregar
mi_lista.append()#Podemos Agregar algo a la lista.

#actualizar
mi_lista[0] = 'alfa'#Esto lo que haca es actualzar la lista

# Eliminar elementos
mi_lista.pop(index)# Elimina un elemento y si no agregas nada se elimina el ultimo.
```


Podemos usar [[Metodo index|index]] y [[Extraer Sub-strings|Slicing]] en las listas

### Métodos en listas

```python
mi_lista = [10,"hola",True,5.2]
len(mi_lista)#Cuenta cuantos elementos hay

# Ordenar la lista
mi_lista.sort()#no devuelve nada solo se ordena.

#Ordenar al revez
mi_lista.reverse()#No se puede almacenar por que no retorna nada.

```

