---
Author: You Tube
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
# Mover archivos

```python
import shutil
# Tambien se puede renombrar el archivo cuando lo mueves
shutil.move(path_nombre_directorio, directorio_destino)
```


# Copiar archivos

```python
import shutil
# Tambien se puede renombrar el archivo
shutil.copy(path_nombre_directorio + nombre, directorio_destino + nombre)
```

# Eliminar directorios 

```python
import shutil
# eliminar directorios
shutil.rmtree(path_directorio)

```
# eliminar archivos

lo tenemos en [[directorios]]