---
Author: Christian laurean
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Entorno_antes_proyectos]]"
---
- `which python3`: donde se ejecuta python
- `which`

# instalar el entorno virtual

`sudo apt install -y python3-venv`

# Crear el ambiente

`python3 -m venv env`

# activar el ambiente

`source env/bin/activate`

# salir del entorno virtual

`deactivate`

# ver los módulos que tenemos instalados

`pip3 freeze`

# instalar 

`pip install nombre`

# requirements.txt

Aquí ponemos todo los módulos que tenemos instalados para que otros lo puedan leer.

`touch requirements.txt`

## Generar el archivo con el siguiente comando

- `pip3 freeze > requirements.txt`

## Revisar lo que hay dentro del archivo

- `cat requirements.txt`

Instalar las dependencias necesarias para contribuir más rápido en proyectos

- `pip3 install -r requirements.txt`
