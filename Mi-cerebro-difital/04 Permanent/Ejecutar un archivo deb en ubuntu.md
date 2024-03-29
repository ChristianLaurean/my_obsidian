---
Author: You Tube
Category: Linux
Type: Apunte
Status: Terminado
relación: "[[Terminal de Linux]]"
---
```bash
dpkg -i paquete.deb
# o y me a funcionado bien es:
sudo apt install ./iriunwebcam-2.8.1.deb
```

Desistalar 
```bash
1. Abre una terminal.
    
2. Ubica el nombre del paquete que deseas desinstalar. Puedes obtener una lista de los paquetes instalados usando el siguiente comando:
    
    bashCopy code
    
    `dpkg -l | grep nombre_del_paquete`
    
    Sustituye "nombre_del_paquete" con el nombre real del paquete que deseas desinstalar.
    
3. Una vez que hayas identificado el nombre del paquete, utiliza el siguiente comando para desinstalarlo:
    
    bashCopy code
    
    `sudo dpkg -r nombre_del_paquete`
    
    Esto eliminará el paquete, pero conservará sus archivos de configuración. Si deseas eliminar también los archivos de configuración, utiliza el siguiente comando:
    
    bashCopy code
    
    `sudo dpkg -P nombre_del_paquete`
    
    Ten en cuenta que la opción `-P` eliminará también los archivos de configuración del paquete.
```