

# Funciones

>[!tip] Las funciones sirven
>Sirven para crear bloques de código, y así poder reutilizar un bloque de código en especial al código o al proceso que queremos hacer

# Manipulación de strings para el procesamiento de datos

Es una orden de una base de datos pero todo esta en un tipo de datos strings tenemos que solucionarlo

```python
order = '1,2022-10-01, 1, COMPLETE'
```

### La función `split`

>[!tip] Las funcion sirven
>Sirven para dividir un strings y lo retorna en una lista con los datos ya divididos.
>`order.split(',')` Con esto se divide y si no le agregamos nada se divide por espacios  

## Otrass funciones
```python
len(order) #cuenta los caracteres o cuantas colecciones tiene una lista
sum(list_order)#Puedes sumar todos los datos enteros de una lista
```

# Procesamiento de datos con map y filter

## Lambda function

>[!tip] que es?
>Es una función sin nombre 

```python
def sum(n):
	return 5 + n

funti = lambda n : n + 5
funti(1)# 6

# Podemos usarlo en list o dict comprehesion
list_data = [lambda n : n + 5 for n in data]
```

## MAP

>[!tip] Es una función que itera y convierte los datos a otro tipo de datos
>map recibe dos argumentos **funcion** y un **iterable** y devuelve un objeto
>`map(func, *iterables) --> object`
>La función(**lambda**) aplicara todas las trasformaciones del iterable

## FILTER

>[!tip] Es una función que itera y filtra los datos
>filter recibe una **función** o no recibe ni una y un iterable
>`filter(func or none, *iterables) --> object`
>`filtrado = list(filter(lambda n : n.split(',')[3] == 'COMPLETE', orders))`
>La función(**lambda**) aplicara todos los filtros

## sorted

>[!tip] Es una función que ordena los resultados
>`sorted` itera y devuelve una lista ordenada
>`sorted(iterable, key=None, reverse=False) --> object`
>`sorted(orders,key=lambda n : int(n.split(',')[2]),reverse=True)`
>La función sorded itera la lista orders, busca el keys lo trasforma

# Archivos json

>[!tip] Para que sirve
>Los archivos json son estructuras que nos van a regresar como respuesta de un servidor y para un [[200 - Data Engineer|Data Engineer]] Es muy importante saber procesarlos.

Para poder manipar archivos json debemos usar el modulo json
```python
data = json.loads(variable_json) # Esto convertira el archivo json a un diccionario o lista
```

## Procesando json para metadatos

```python
import json

def get_json():

    with open(file_path) as file_json:

        return json.load(file_json)

  

def get_columns(schema,dataset,colum_name):

    g = sorted(schema[dataset], key= lambda n: n[colum_name])

    return list(map(lambda n : n[colum_name],g))

schemas = get_json()

print(get_columns(schemas,'orders','column_name'))
```


# Pandas

>[!example] codigo pandas
>`import pandas as pd` # importamos la libreria
>Podemos leer muchos archivos y bases de datos

## Leer archivos CSV
```python
pd.read_csv(path,sep="como separarlos datos",header="ingresa un numero entero Cual se usa como columnas",names='colocamos los nombres dekas cikymnas en lista')

```

## filtrar datos con pandas

```python
orders['order_status'] # Filtramos solo esa columna

orders['order_status'].unique() # nos da valores unicos

orders['order_status'].query('order_status == "COMPLETE" and date_order == "2014-01-01 00:00:00.0"') # Con esto podemos filtrar y hacer una consulta
```

## Agregaciones con pandas

```python
csv_file.groupby('columna').agg('count') # agrupamos una columna del dataset y agregamos la agregación que queramos pero todas las columas van a contarse.
# ---------------------------------------------------------------------
csv_file.groupby('columna')['columna_que se va a contar o sumar'].agg(order_count='count') # Ahora la agregación se hace en una sola columna.

# ---------------------------------------------------------------------
# Doble agrupación
csv_file.groupby(['meses','order_status'])['id_order'].agg(order_count='count').reset_index()
```

## Funciones con pandas


```python
# Apply se usa para las trasformaciones a nivel de fila y columna
csv_file['meses'] = csv_file.apply(lambda csv_file : csv_file.date_order[:7], axis=1) # Lo que hace es crear una nueva columna llamada meses, despues hacemos una trasformación a nivel de filas y usamos aply para eso, despues se va a iterar y ponemos la columa que queremos trasformar, agregamos axis=1 para que busque las columnas por los nombres y si es 0 buscara por el indice por filas.
```

## Unir tablas

1. Debemos de ver que columnas se relacionan o quieres relacionar, Después usar esa columna como index para poderlas relacionar y lo hacemos con: 

```python
custumer = df_custumer.set_index('customer_id')
orders = df_order.set_index('order_customer_id')
```

2. Ya que tenemos las columnas en el index ahora podemos relacionarla con `join`
```python
df.join(segundo_df, 
		on=nombre_de_indice(pordefecto),
		how='el_tipo_union_que_quieres'
		)
```

Ejemplo:
```python
custumer_orders = custumer.join(orders, how='inner')
custumer_orders.reset_index().\
    groupby('customer_id')['order_id'].\
    agg(contar='count').\
    reset_index().\
    query('contar >= 15').\
    sort_values('contar', ascending=False)
```


## Ordenar datos con pandas

ordenar por columnas
`df.sort_values('colum_df', ascending=False)`

```python
custumer_orders = custumer.join(orders, how='inner')
custumer_orders.reset_index().\
    groupby('customer_id')['order_id'].\
    agg(contar='count').\
    reset_index().\
    query('contar >= 15').\
    sort_values(['contar','colum2'], ascending=[False, True])
```

## importar dataset con pandas

### CSV

```python
custumer_orders.to_csv('path_archive',sep=','(predeterminado),columns=['lista_nombre_columnas'])
```

### Json


```python
# read
pd.read_json('file',lines=True)
# ecritura -----------------------------------------------------
custumer_orders.to_json('path_archive',orient='Guarda los datos en registro(records)',lines='Permite un booleano True en formato registro', index='Es un bool para ver si queremos almacenar los indices')
```

# Proyecto

## variables globales
```python
import glob
glob.glob('path', recursive=bool)
glob.glob('path**', recursive=bool) # nos da todas las carpetas y archivos en una lista.
glob.glob('path/*/*') # nos da todos los archivos que esten dentro de una carpeta
```

## Expresiones regulares

```pyton
import re
re.split('[delimitadores]', lista)
```

# Dependencias
```bash
python3 -m venv entorno-venv
```
Para escoger un entorno `ctr + p` `Python:Slect interprete`
## instalar dependencias

```bash
source tutorial-env/bin/activate
pip install pandas

# Crea un archivo requeriments
pip freeze > requirements.txt

```

# buenas practicas



## SDLC

>[!tip] Que es SDLC?
>Ciclo de vida de desarrollo de software
>El desarrollo de nuestra app pasa por direfentes fases
> - Fase de prueba de desarrollo
> - Produccion 


## sys
`ìmport sys `
Es un modulo que nos permite darle argumentos desde la terminal y esto hace mas robusto la aplicación

```python
sys.argv
```

# Manejo de errores


# insertar tablas a otra base de datos


### Dependencias que se ocupan
`ipython-sql`: Es una extensión SQL
```python
%load_ext sql # Carga dependencias externas que usaremos

%env DATABASE_URL=postgresql://name:paswword@localhost:puerto/nombrebasededatos

Para leer el env:
%env DATABASE_URL
```

`psycopg2-binary` Solo me sirve por que lo ocupa pandas junto con `sqlalchemy`


### Conectarme con pandas

```python
import pandas as pd

conn_url = 'postgresql://chris:Milito21@localhost:5432/itversity_retail_db'

pd.read_sql(sql(querys),con)
```

# exportar sql

```python
df.to_sql('table',conn,if_exists='replace', index=False,chunksize=10000)
```
`method(None,'multi','callable')`
`None: Creara Todos los insert que se necesitan`
## chucksize
```python
# Nos ayuda a procemar mejor los datos por que los dividimos

df_reader = pd.read_csv('path',names_columns,chunksize=10000)
# Nos devuelve un tipo de dato TeztFileRader y es como una lista
```


# Solucionar problemas con python

1. Problemas de conectividad a una [[base de datos]] 
2. Errores de tiempo de compilación(Errores de sintaxis)
3. Errores de tiempo o exceptiones
4. busg del condigo de python
5. Problemas de optimización

## Detalles para depurar los errores

1. Leer el error correctamente
2. Comprender que esta pasando
3. tomar el suficiente tiempo para pensar en como solucionar el problema de raiz
4. Ya visto cual es es muy fácil solucionarlo

### Problemas de conectividad

1. Problemas con el puerto:
	1. Puede ser un firewaill que esta bloqueando el trafico extremo
	2. **Solución**: Trabajar con el equipo de redes para ese problema
2. Problemas de sintaxis
	1. Leer bien el error para saber en donde esta ese error de sintaxis

### Problemas de compilación y ejecución
1. Python siempre compila y después ejecuta 
	1. Si tiene errores python jamas se va a ejecutar python por que hay errores en la compilación
### Problemas de tiempo de ejecución

1. Son exepciones que pasan en python y esto se soluciona manejando esos errores
2. Son cuando ya python esta en ejecución

### Busgs
#### Estapas de vida del sofware
1. Requerimientos
2. Diseño 
3. Desarrollo(uni testing)
4. (QA)
5. Production

Podemos depurar el código con visual code




#### Como funciona python con SQL
Puede haber varios servidores en una app determinada y esos tienen bases de datos

# Mejorar el rendimiento a aplicaciones con python

Antes de entrar a rendimiento debemos saber:
1. Revisar la configuración del sistema en la que se va ejecutar la app
2. Comprender la carga del trabajo
3. Comprender las caracteristicas de la aplicación osea como se ecjecuta osea cuellos de botella
4. Entender SLAs

1. Run app
	1. Saber si la aplicación no satisface los requisitos o si
	2. si no debemos hacer soluciones para que si
2. identificar los cuellos de botella
	1. Tenemos tres fases extract, trasform y target que si vemos que una de esas partes dura mucho tiempo debemos de ver como aumentar el rendimiento
	2. Tiempo CPU, Cantidad de I/O y reducir el tiempo general eso se considerar mejorar el rendimiento

Cuando ejecutamos una app usamos CPU y memoria ram y python crea mucho objetos y esos requieren memoria y cuando procesamos los datos se requiere CPU
objeto = al read de pandas.
y ese dataframe se leera en memoria Pero si usamos chunksize ahora es otro tipo de objeto de tipo texto entonces solo usara la memoria necesaria de cada chunk a la hora de procesar y ya que se procesar entonces se elimina en memoria

## Multiprocesing

Usamos multiples procesadores en un servidor determinado para procesar los datos en paralelo

```python
import multiprocessing
# Es una clase
# instanciamos la clase

pool = multiprocessing.Pool(4) # el numero es usar cuatro procesos en paralelo para procesar datos

pool.map(funcion, iteración) # --> Devuelve una lista

```

Como funciona

![[Pasted image 20231216095024.png]]
Resumen

1. Para el modo lectura usar Chunksize con pandas
2. Para el modo escritura usar chunksize
3. Usar multiprocesamiento
4. Agregar indices a la foreig keys para que las uniones funcionen bien
5. Pasar consultas por que usara los recursos de la base de datos