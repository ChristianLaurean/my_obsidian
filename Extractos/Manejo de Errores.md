---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
`try` Intenta ejecutar el cogido
`except` Si pasa algo malo, mejor haz otra cosa
`finaly` No importa si hay un error, ejecuta esto

```Python
try:
	codigo_queremos_probar
except:
	#Codigo_ejecutar si no hay error
else: 
	# Ejecutar si no hay error
finally:
	#Codigo que se va a ejecutar todos modos
```

Necesitamos que se pare el procesamiento de datos cuando un archivo sea 0 para eso usamos `raise`

```python
raise NameError('Mensaje que quieras')
# Lo podemos usar en una función y despues usar Try: Except
# ---------------
```


