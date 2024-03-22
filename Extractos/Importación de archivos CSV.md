---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
# archivos CSV usando [[Pandas]]

```python
pd.read_csv('Divvy_Trips_2018_Q4.csv'
```

---
### Parámetros de `read_csv`

`sep=` Como separar el archivo csv

`header` Si tiene columnas y en  que posición están o si no tiene.

`names` se utiliza para especificar los nombres de las columnas del DataFrame.

`nrows` El numero de filas que quieres ver.

`skiprows` Numero de filas que te quieres saltar
- `nrows` se usa en combinación de : `skiprows` por que es el numero de filas que quieres ignorar al inicio

`usecols` Se utiliza para especificar qué columnas del archivo CSV deben ser cargadas en el DataFrame.
- `pd.read_csv('Divvy_Trips_2018_Q4.csv',usecols=names_col)`

`dtypes` Es un diccionario donde le pasamos el nombre de la columna como KEY y el valor es el tipo de dato. y nos ayuda a cambiar el tipo de dato.
- `pd.read_csv('Divvy_Trips_2018_Q4.csv',dtypes={"columna":str})`

`comment` Nos sirve para ignorar y no cargara esos comentarios
- `pd.read_csv('Divvy_Trips_2018_Q4.csv',comment="#")`

`na_values` se utiliza para especificar los valores que deben considerarse como valores
- `pd.read_csv('Divvy_Trips_2018_Q4.csv',na_values)`

# archivos csv desde la web

```python
# Assign url of file: url

url = "https://assets.datacamp.com/production/course_1606/datasets/winequality-red.csv"
# Read file into a DataFrame: df

df = pd.read_csv(url,sep=";")
```

