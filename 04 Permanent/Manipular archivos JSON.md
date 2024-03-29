---
Author: You Tube
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# JSON

>[!tip] Es un formato ligero para su almacenamiento de información 
>Con este nos podemos enviar como recibir información
>Podemos persistir información
>Es como un [[Diccionarios]]


## Convertir el objetos json a diccionario

```python
import json

json_file = {}
user = json.loads(json_file)# recibe el objeto json y lo convierte en diccionario
```

## Diccionario a un objeto json

```python
import json

dict_file = {
	'name':'chris',
	'email':'email@gma.cpm'
}

json_object = json.dumps(dict_file)# retorna un string
```

## Leer archivos con extensión .json

```python
import json

with open('file_json') as file:
	payload = json.load(file)# convertimos el objeto json a diccionario 
```

## Crear archivos Json

```python
import json

with open('file_json.json', w) as file:
	json.dump(lista_diccionario,file, indent=2)
```