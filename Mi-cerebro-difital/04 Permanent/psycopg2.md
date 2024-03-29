---
Author: Christian laurean
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Python]]"
---
- ¿Qué es psycopg2?
    - Es un adaptador de base de datos PostgreSQL para Python.
- ¿Por qué usar psycopg2 con Python?
    - Es rápido, eficiente y permite interactuar fácilmente con bases de datos PostgreSQL desde Python.
- Instalación de psycopg2
    - `pip install psycopg2`
### Conexión a una base de datos PostgreSQL
```python
import psycopg2

try:
    conn = psycopg2.connect(
        dbname="nombre_basedatos",
        user="usuario",
        password="contraseña",
        host="localhost",
        port="5432"
    )
    print("Conexión exitosa")
except psycopg2.Error as e:
    print("Error al conectar a la base de datos:", e)
finally:
    conn.close()
```

### Ejecución de consultas SQL

```python
cursor = conn.cursor()
cursor.execute("SELECT * FROM tabla")
rows = cursor.fetchall()
for row in rows:
    print(row)
```

### Recuperación de datos de la base de datos

```python
cursor.execute("SELECT nombre, edad FROM personas WHERE ciudad = %s", ('New York',))
row = cursor.fetchone()
# Todos los elementos
row = cursor.fetchall()
print("Nombre:", row[0])
print("Edad:", row[1])
```
### Manejo de transacciones

```python
try:
    conn.autocommit = False
    cursor.execute("INSERT INTO tabla (columna) VALUES (%s)", ('valor',))
    conn.commit()
except psycopg2.Error as e:
    print("Error en la transacción:", e)
    conn.rollback()
finally:
    conn.autocommit = True

```

### Cierre de la conexión y limpieza

```python
cursor.close()
conn.close()
```

```python
import psycopg2

try:
    with psycopg2.connect(
            dbname="nombre_basedatos",
            user="usuario",
            password="contraseña",
            host="localhost",
            port="5432"
    ) as conn:
        print("Conexión exitosa")
        
        with conn.cursor() as cursor:
            cursor.execute("SELECT * FROM tabla")
            rows = cursor.fetchall()
            for row in rows:
                print(row)
                
except psycopg2.Error as e:
    print("Error al conectar a la base de datos:", e)
```
 O como dice coderhouse
 ```python
 import psycopg2

# Suponiendo que DNS y SQL ya están definidos

with psycopg2.connect(DNS) as conn:
    with conn.cursor() as curs:
        curs.execute(SQL)
```