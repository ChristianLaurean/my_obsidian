---
Author: Coderhouse
Category: Entorno
Type: Apunte
Status: Terminado
relación: "[[Bibliografia/Docker|Docker]]"
---
# Maquinas virtuales

Es una capa de abstracción que permite correr un sistema operativo sobre una máquina con un sistema operativo diferente.

## Como interactua la maquina física con la maquina virtual.

#### **[[Hypervisor]]**
Es una capa de [[Software]] que permite administrar los recursos de la maquinas física para compartiselo a la maquina virtual.
Hay dos tipos de [[[Hypervisor]]]
- **Bare metal**
	- interactua con el hardware y los recursos del usuario 
- **Virtual Machine Monitors**
	- Ejecuta un programa en el sistema operativo físico.
	- por ejemplo los programas para virtual-izar maquinas virtuales

>[!sucees] Ventajas
>- Uso eficiente de los recursos de la maquina física.
>- Escalabilidad: por que podemos definir cuantos recursos necesitamos de la maquina fisica. 
>- Gestión eficiente del tiempo 
>- Recuperación más rápida de nuestros sistemas por si falla

![[Pasted image 20240316092509.png]]














