---
Author: You Tube
Category: Linux
Type: Apunte
Status: Terminado
relación: "[[Terminal de Linux]]"
---
Sirve para poder automatizar comandos y tareas

```bash
crontab -l # Para ver si tengo crontab

#crear
crontab -e

```

```bash
* * * * * cd /home/christianlaurean/Documentos/practica/api_noticias/ && . env/bin/activate && /home/christianlaurean/Documentos/practica/api_noticias/env/bin/python /home/christianlaurean/Documentos/practica/api_noticias/main.py
```

Para que se ejecute un programa con python es:

1. movernos a la carpeta
	`cd /home/christianlaurean/Documentos/practica/api_noticias/`
2. Activar el entorno viartual
	`. env/bin/activate`
3. buscara el ejecutable de python
	`/home/christianlaurean/Documentos/practica/api_noticias/env/bin/python`
4. ejecuta el prgrama
	`/home/christianlaurean/Documentos/practica/api_noticias/main.py `
	


# otra forma

- Crear un archivo .sh
- En el archivo
	- `#! /bin/bash`
	- `cd dirección_donde_esta_el_ejecutable_python_main.py
	- `source env/bin/activate`
	- `cd dirección_donde_esta_el_ejecutable_de env
![[Pasted image 20240122122335.png]]
- Tenemos que darle permido chmod +x archivo.sh
- Para probarlo: ./ archivo.sh
en crontab
* * * * * /home/christianlaurean/Documentos/practica/api/ne.sh
