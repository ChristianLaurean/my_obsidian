---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# Metodos de strings

- [[Metodo index]]
- [[Formatear Cadenas]]
- [[Extraer Sub-strings]]

## strings a mayúsculas

```python
texto = "Este es el texto de christian"
texto[2].upper()# podemos usar [[Metodo index]] 
resultado = texto.upper()
```
## strings a minúsculas

```python
texto = "Este es el texto de christian"
resultado = texto.lower()
```

## Separar partes un carácter

```python
texto = "Este es el texto de christian"
resultado = texto.split()# Separa los elementos y los guarda en una lista.
# Podemos agregarle cuelquier separador que queramos
```

## unir items usando un separador

```python
texto = ["Este es el texto de christian","tambien se llama"]
e = " ".join(texto)#Todo lo que tenga adentro del parentecis lo va a unir y lo separa por espacios.
#esto convierte una lista en [[strings]]
```

## encontrar sub-strings

```python
texto = "Este es el texto de christian"
resultado = texto.find("s")#Busca un caracter de nuestro string
# si no existe el string no nos da error.
```
## remplazar strings

```python
texto = "Este es el texto de christian"
resultado = texto.replace(" ", "c")#("texto_eliminar","texto_remplazar")
```

### PDF de todos los métodos de los strings

file:///home/christianlaurean/Descargas/M%C3%A9todos+de+Strings.pdf
