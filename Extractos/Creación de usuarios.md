---
Author: Coderhouse
Category: Bases de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# Permisos

### Nivel usuario 
Se le puede dar un permiso a un usuario



# Crear usuarios 

```sql
-- Usuario sin contraseña y sin limite de uso
CREATE user nombre_usuario password disiable valid until 'infinity'
-- Usuario con contraseña y valido hasta una fecha
CREATE user nombre_usuario with password 'contraseña' valid until '2024-12-12'
```

### Manejo de usuarios

```sql
-- hacerlo superusuario y debe de tener una contraseña
ALTER user nombre_usuario createuser
```

# DCL

- Data
- Control
- Language

## Tipos de permisos
- [[SELECT]]: Es que se pueda dar permisos de consultas
- [[UPDATE]]: Le damos permisos de actualizar registros
- [[DELETE]]: Le damos permisos de eliminar registros o también borrar el objetos.
- [[INSERT]]: Permisos para que puedan insertar nuevos registros
- REFERENCES: Vamos a poder manejar o administrar las [[Primary key]] o [[Foreign keys]] que tenga la tabla.
- TEMPORARY: Permisos para objetos temporales 
- USAGE: Permisos para cualquier objeto de la base de datos
#### Dar permisos de tablas

```sql
-- Darle permisos de lectura en una tabla de la DB
GRANT SELECT ON TABLE nombre_tabla to nombre_usuario

-- Darle todos los permisos
GRANT ALL ON TABLE nombre_tabla to nombre_usuario
```

##### Quitar permisos

```sql
-- quitamos permisos
REVOKE select on table nombre_tabla from nombre_usuario
```

### Buena practica y consejos
- tener un control preciso de quien tiene un permisos a nuestra base de datos y que permisos tiene
-  Dar el mínimo permiso.
- Jamas darle todos los permisos que se pueden dar a una sola persona.

## Permidos a Nivel de grupo y Roles
Se le da permiso a nivel de una área de la empresa o trabajo.