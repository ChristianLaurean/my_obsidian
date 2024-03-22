---
Author: DataCAMP
Category: Bases de datos
Type: Apunte
Status: Terminado
relación: "[[Fundamentos de Bases de datos]]"
---
Un registro que hace referencia a otro registro en otra tabla siempre debe hacer referencia a un registro existente.

>[! warning] Un registro de la tabla A no debe de hacer referencia a un registro de la Tabla B que no existe.


- ON DELETE NO ACTION 
	- Si eliminas un registro de la tabla A no pasara nada entonces no habrá integridad referencial
- ON DELETE CASCADE
	- Si elimino un dato de la Tabla A entonces también se elimina el dato de referencia de la tabla B
- ON DELETE RESTRICT
	- Es parecida a NO ACTION
- ON DELETE SET NULL
	- Si elimino un dato de la tabla A entonces en la Tabla B se crea NULL
- ON DELETE SET DEFAULT