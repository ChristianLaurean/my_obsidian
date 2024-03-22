---
Author: Coderhouse
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Docker|Docker]]"
---
1. Tener todas nuestras actualizaciones instaladas 
	```Bash
	sudo apt-get update
	sudo apt-get upgrade
	``` 
2. Actualizar
	```Bash
	sudo apt update
	sudo apt upgrade
	``` 
3. instalar paquetes en el sistema para que se permita la trasferencia de información de lo que es docker
	```Bash
	sudo apt install apt-transport-https ca-certificates curl software-properties-common
	``` 
	- **apt-transport-https**: Se usa para permitir conexiones HTTP con repositorios seguros
	- **ca-certificates**: Permite chequear la autenticidad de certificado SSL
	- **curl**: permite la trasferencia de archivos
	- **software-properties-common**: Permite manejar tu distribución como un sofware independiente
4. Agregar la GPG KEY al sistema operativo
	```bash
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
	```
	- curl -fsSL: Permite la descarga silenciosa de una URL y muestra errores cuando ocurren
	- sudo apt-key add -: permite agregar y descargar las keys de OpenPGP para auntenticación
6. Agregar el docker repository
	```bash
	sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

sudo apt install docker-ce
docker --version
	```