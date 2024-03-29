---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
# SQLite

`create_engine` Nos ayuda a crear un motor de SQL que comunicara las consultas a la [[Base de datos]]

```python
from sqlalchemy import create_engine
engine = create_engine("sqlite:///Nnorthwing.sqlite")
```

### Saber el nombre de las tablas 

```python
table_names = engine.table_names()
print(table_names) -> #lista con los nombres de las tablas
```

# querys a la base de datos.

```python
QUERY = """ 
SELECT * 
FROM table
"""
from sqlalchemy import create_engine
engine = create_engine("sqlite:///Nnorthwing.sqlite")
con = engine.connect() conexion al motor
rs = con.execute(QUERY)
rs.fetchall() -> Es una lista que cada fila es una tupla de todos los datos.

df = pf.DataFrame(rs.fetchall())
# si no tiene columnas podemos agregarlas asi:
df.columns = rs.keys()
con.close()
```
`fetchall()` -> Todos los datos
`fetchmany(size=5)` -> Las filas que le pida. 

## conexión con contexto

```python
engine = create_engine("sqlite:///Nnorthwing.sqlite")
with engine.connect() as con:
	rs = con.execute(QUERY)
	df = pf.DataFrame(rs.fetchall())
	df.columns = rs.keys()
#  con esto ya no nos preocupamos por cerrar la conexión
```

## CON [[Introducción a Pandas]]

```python
engine = create_engine("sqlite:///datasets/Chinook.sqlite")

df = pd.read_sql_query(query,engine)
df
```