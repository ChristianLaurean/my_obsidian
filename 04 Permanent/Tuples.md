---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# Que son las tuplas?
>[!tip] Son una colección de elementos iguales que las listas solo que son inmutables osea que no se pueden cambiar y son mas rápidas para la lectura.
>```python
>mi_tuple = ("hola",1,True,5.5)
>```
>Podemos tener todos los tipos de datos
>- Podemos usar [[Metodo index|index]]
>- Podemos usar [[Extraer Sub-strings|slicing]]
>- Podemos anidar tuplas


```Python
# consultar información
mi_tuple[0]

# Podemos convertirla a lista y de lista a tupla
mi_lista = list(mi_tuple)
mi_tuple = tuple(mi_lista)
```

### Desempaquetar Tuplas

También lo podemos hacer con [[Listas]] y [[Diccionarios]]
```Python
mi_tuple = (1,2,3)
x,y,l = t
print(x,y,l)#1 2 3 Se asigna elemento por elemento y deben de ser los mismo valores
```
