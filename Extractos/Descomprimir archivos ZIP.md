---
Author: Christian laurean
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
```Python
import zipfile


def extract_zip(path_name, path_destination):
    with zipfile.ZipFile(path_name, 'r') as zip_file:
        zip_file.extractall(path_destination)# Se crea una carpeta y se descomprime los archivos ahi no hay necesidad de ponerle el tipo de archivo.
        zip_file.extract(ruta)# solos se descomprime sin carpetas
```