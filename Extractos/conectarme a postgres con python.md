---
Author: You Tube
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de SQL]]"
---
# instalar
`pip install psycopg2`

```python
import psycopg2

conn = psycopg2.connect(host="localhost", dbname="nombre_db", user="",password='123',port=5432 )

cur = conn.cursor()
```

`cur.fetchone()` nos trae la respuesta por ejemplo un select
`cur.close()`
`cunn.close()`
## Crear Tablas
[[Creación de Tablas]]
```python
cur.execute("""CREATE TABLE IF NOT EXISTS table ()""")
conn.commit()
```

## insertar datos

[[INSERT]]
debemos ponerle una [[Tuples]]
```python
cur.execute("""INSERT INTO table () VALUES (%s, %s, %s)""", tupla_datos)

# insertar muchos datos
Lista_tuplas = [()]
cur.executemany("""INSERT INTO table () VALUES (%s, %s, %s)""", lista_tuplas)

```
