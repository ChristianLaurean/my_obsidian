---
Author: Coderhouse
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
# archivos planos con numpy

```python
import numpy as np
filename = "archivo.txt"
data = no.loadtxt(filename, delimiter',',skiprows=1#omitimos una row)
# usecols necesita una lista para extraer las columnas que quiera
data = np.loadtxt(file, delimiter="\t", skiprows=1, usecols=[0,2])

# podemos hacer que todos los datos sean str
data = no.loadtxt(filename, delimiter',',dtype=str)

# La mejor manera es:
data = np.genfromtxt('titanic.csv', delimiter=',', names=True, dtype=None)
```


>[!warning] No es tan buena idea usarlo si el archivo tiene muchas incositencias


# Lectura de archivos CSV y json



---



# json

```python
df = pd.read_json('ruta.json',orient="split")
df
```

## APis

```python
response = requests.get(url)
response.raise_for_status()
population = response.json()
# Crear DataFrame
pd.DataFrame(population[1])
```

### Aplanar json anidados

```python
pandas.io.json
json_normalize()
```
![[Pasted image 20240227173942.png]]

## Extraer datos de una base de datos

```python
read_sql_query('query',conn)
```

```python
import psycopg2
conn = psycopg2.connect(dbname='nombre_db',user='name',password='contraseña',host='host',port='5414')
cur = conn.cursor()#nos permite hacer querys