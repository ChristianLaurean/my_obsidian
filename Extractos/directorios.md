---
Author: Udemy
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# Método pathlib

```python
from pathlib import Path
from pathlib import Path, PureWindowsPath # Es lo mismo pero para windows

carpeta_actual = Path.home()#directorio home

carpeta_actual = Path.cwd()#directorio actual
carpeta = Path('/home/documentos')
carpeta = Path('home','documentos') # nueva_ruta
path_currem = carpeta / "estudio" / "python"

print(carpeta.name)#imprimimos el nombre del archivo o directorio con todo
print(carpeta.suffix)#imprimimos la terminación del archivo
print(carpeta.stem)#imprimimos el nombre del archivo sin la terminación
print(carpeta.parent)# es como cd ..


# condicionales
carpeta.is_dir()#Es carpeta o no
carpeta.is_file()#es archivo o no
carpeta.is_absolute()# Es una ruta absoluta(con raiz) o no

if not carpeta.exists():# checa si el archivo existe o no.
	print("Ya existe")
#iterar todas las carpetas
for i in file.iterdir()

for txt in Path(ruta).glob("**/*.txt"):
	print(txt)

# Crear carpetas
carpeta.mkdir()#crea carpeta
carpeta.touch()#crea archivo

# eliminar
ruta_archivo.unlink() # eliminar archivos

ruta_directorio.rmdir()# eliminar directorio
```

```python
# limpiar_consola
from os import system('csl')
```