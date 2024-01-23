---
Author: You Tube
Category: Linux
Type: Video
Status: Terminado
relación: "[[Terminal de Linux]]"
---
# APT Y APT-GET

- Vienen instalado en Linux
### Actualizar la lista de repositorios

```bash
# actualiza solo la lista de los repositorios
sudo apt-get update
# actualiza los repositorios
sudo apt-get upgrade
```

### Instalar nuevos paquetes

```bash
sudo apt-get install
```

### desistalar paquetes

```bash
# Solo elimina el programa
sudo apt-get remove
# Elimina el programa y archivos de configuración que creo el repositorio
sudo apt-get purge
```

# APTITUDE

- Se tiene que instalar
	- `sudo apt-get install aptitude`
- Version mejorada de apt-get
- Al eliminar un paquete, elimina las dependencias
- **Siempre pregunta, antes de hacer algo**

### Actualizar la lista de repositorio

```bash
sudo aptitude update
sudo aptitude upgrade
```

### instalar repositorio

```bash
aptitude search nombre_repositorio

# isntalar
sudo aptitude install nombre repositorio
```

### desistalar el repositorio

```bash

sudo aptitude remove nombre_repositorio
# elimina dependencias y carpetas de configuración
sudo aptitude purge nombre_repositorio
```