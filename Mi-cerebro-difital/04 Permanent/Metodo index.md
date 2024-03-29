---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
Es un método para un [[strings]]
# index

Lee de Izquierda a derecha y empieza en 0

![[Pasted image 20240105104923.png]]
AL revés
![[Pasted image 20240105105029.png]]

>[!tip] Para que sirve?
>Para saber donde se encuentra un caracter
>```python
>mi_texto = "Hola"
>mi_texto.index("o")#Posición 1
>```
>Que caracter existe en una determinada posición
>```python
>mi_texto = "Hola"
>mi_texto[3] # a
>```

## Parámetros adicionales de index

```python
mi_texto = "Hola"
mi_texto.index("o",5,10)#index.(letra_buscar,donde empieza a buscar, donde finaliza)
```

## Método rindex()

>[!tip] Que hace?
>Es lo mismo que index solo que busca al revés de derecha a izquierda

