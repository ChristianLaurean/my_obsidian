---
Author: Platzi
Category: Limpieza de datos
Type: Apunte
Status: 
relación: "[[Terminal de Linux]]"
cssclasses:
  - page-white
---
Tenemos una entrada que se le llama standar input(0) y lo que muestra en la linea de comandos es el standar outputh(1) O el standar Error(2).
![[Pasted image 20240411090435.png]]

- stdin (0): Entrada estándar.
- stdout (1): Salida estándar.
- stderr (2): Salida de errores.

Redirige el input de un comando hacia un archivo.

```bash
comando < archivo
```

Redirige la salida de un comando a un archivo. El mismo sobrescribe el contenido del archivo a donde se redirige la salida.
```bash
comando > archivo
```

Concatena la salida de un comando a un archivo. Si no existe el archivo lo crea.

```bash
comando >> archivo
```

Redirige la salida de error de un comando a un archivo.

```bash
comando 2> archivo
```

Redirige la salida de un comando, que se ejecuto satisfactoriamente o un comando que presento errores, a un archivo.

```bash
comando > archivo 2>&1](<```bash
```
