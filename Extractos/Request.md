---
Author: You Tube
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de APis]]"
---
>[!tip] Instalar la libreria Request
>```bash 
>python3 -m venv env
>source env/bin/activate
>pip install requests
>```



# GET

```Python
import requests

url = 'https://api.imgflip.com/get_memes'
#nos ayuda a hacer que la respuesta se comprima y eso hacer que la descarga sea mas rapida.
headers = {"Accept-Encoding": "gzip, deflate"}

#Retorna un objeto tipo response
response = requests.get(url)
print(response)
print(response.status_code)# Saber el estus del servidor
print(response.text)#Saber el cuerpo de la respuesta y es un str.
r = response.json()
print(r['data']['memes'][0]['url'])#Serializar el objeto y poderlo manupular.
```

# Params

Permite enviar información al servidor con la url

```python
# Se le llama query
# Es todo lo que va despues del ?
# Las variables se separan por &
url = 'https://api.imgflip.com/get_memes?query&query'
params = {
	'name':'query',
	'password': 123
}

request.get(url,params=params)
```

# Headers

 Para enviar metadata al [[Servidor]]

```python
headers = {
		   'curso':'programación',
		   'version':2.0
}

reponse.get(url,headers=headers,params=params)
```

## descargar archivos

```python
# No se cierre la conexión del servidor hazta que se descarge y se descarga en chunks.

response = requests.get(url,stream=True)
# WB:escritura binaria
with open('img.jpg', 'wb') AS file:
	for chunk in response.iter_content(1024):#kilobites
		file.write(chunk)
```

