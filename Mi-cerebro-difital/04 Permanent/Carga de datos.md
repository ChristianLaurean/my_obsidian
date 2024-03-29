---
Author: Coderhouse
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
# redshift

`sqlAlchemy` : Nos permite conectarnos a una base de datos
- ORM : Administrador de objetos y relaciones.
- Se usa mucho en el desarrollo web.
- no lo usamos mucho
- ALTO nivel
#### usos
- Para hacer querys
`psycopg`: Nos permite usar una base de datos tipo [[PostgreSQL]]
- Es la DBAPI: Es un conectar de base de datos - BBAPI
- Bajo nivel
- Mayor [[Performance]]
`pyodbc`: Es la mas usada y la recomienda el profe
- Mayor uso de la memoria y es mas [[Performance]]
- DBAPI
![[Pasted image 20240308104433.png]]
## instalacion

`pip install SQLAlchemy`
`pip install psycopg2-binary`

## import

`from sqlalchemy import create_enguine` Es una variable que nos permite conectarnos a la [[Base de datos]]

```python
conn = create_enguine('postgresql://usuario:contraseña@host:puerto/nombre_base_datos')

df = pd.DataFrame(Data)
df.to_sql('nombre_equema.nombre_tabla',conn,index=False, if_exists='replace')
```


>[!warning] to_SQL de pandas no es tan escalable es mejor la de spark pero tambien es mas difícil de mantener.
>Es mejor crear nuestra propia libreria
