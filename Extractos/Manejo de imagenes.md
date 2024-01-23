---
Author: Coderhouse
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de APis]]"
---

```bash
pip install Pillow
```




```python
import requests
from PIL import Image
from io import BytesIO
from random import choice

  
  

def get_json(url):
	# Comprime la respuesta del servidor y es mas rapida la descarga
	headers = {"Accept-Encoding": "gzip, deflate"}
#Retorna un objeto tipo response
	response = requests.get(url,headers=headers)
	if response.status_code == 200:
		return response.json()

  

def searsh_meme(file_json):
# list_comprehsion
	list_id_memes = [meme['url']for meme in file_json['data']['memes']]
	
	return choice(list_id_memes)

  

  

def dowload_img(url_meme):
	response = requests.get(url_meme)
	intentos = 0
	print("Descargando imagen")

	while intentos < 5:
		if response.status_code == 200:
# BytesIO Es para hacer visible los bits de la imagen.
			img = Image.open(BytesIO(response.content))
# guardamos la imagen
			img.save("imagen_meme.jpeg", "JPEG")
			print("listo")
			break

		else:
			intentos += 1
			print('intentanto de nuevo...', intentos)

  

if __name__ == '__main__':
	json_file = get_json('https://api.imgflip.com/get_memes')
	url_meme = searsh_meme(json_file)
	dowload_img(url_meme)
```