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

# **_Comprobando errores_**

Como ha visto, el objeto Response tiene un atributo status_code que se puede comparar con request.codes.ok (una variable que tiene el valor entero 200 ) para ver si la descarga se realizó correctamente. Una forma más sencilla de comprobar el éxito es llamar al método rise_for_status() en el objeto Respuesta . Esto generará una excepción si hubo un error al descargar el archivo y no hará nada si la descarga se realizó correctamente. 

```python
res =request.get('https://inventwithpython.com/page_that_does_not_exist')  

res.raise_for_status()
```

El método rise_for_status() es una buena manera de garantizar que un programa se detenga si se produce una descarga incorrecta. Esto es bueno: desea que su programa se detenga tan pronto como ocurra algún error inesperado. Si una descarga fallida _no es_ un factor decisivo para su programa, puede ajustar la línea rise_for_status() con declaraciones try y except para manejar este caso de error sin fallar.

```python
import requests
def get_json():
	url = 'https://api.escuelajs.co/api/v1/produccts'
	res = requests.get(url)
	res.raise_for_status()
	print(res.text)

try:
	get_json()
except Exception as exc:
	print('hubo un problema: %s' % (exc))
```

Llame siempre a rise_for_status() después de llamar a request.get() . Desea asegurarse de que la descarga realmente haya funcionado antes de continuar con el programa.

# encoding

Sirve para cambiar la respuesta o el texto a utf8 

```python
response_text = r.text 
decoded_content = response_text.encode(r.encoding)
```
