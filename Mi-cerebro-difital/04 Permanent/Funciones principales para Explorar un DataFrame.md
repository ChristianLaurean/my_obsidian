---
Author: DataCAMP
Category: Procesamiento de datos
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
cssclasses:
  - center-images
  - center-titles
  - page-manila
  - pen-black
---
- `.Head()` Nos permite ver las primeras filas del DataFrame
	- `df_avocado.head()`

- `.info()` **Muestra los nombres de las columnas, tipos dedatos que contienen y si les falta algún valor**
	- `df_avocado.info()`

- `.shape` **Es un tupla que contiene el número de filas seguidas del número de columnas**
	- `df_avocado.shape # -> es un atributo por eso no tiene parentesis`

- `.describe()` **Calcula algunas estadisticas resumidas para las columnas númericas.**
	- `df_avocado.describe()`

- `.values` **Nos da todos los datos en un [[Array]] de numpy **
	- `df_avocado.values`

- `.columns` **Nos da los nombres de las columnas del df**
	- `df_avocado.columns`

- `.index` **Contiene números de filas o nombres de filas**
	- `df_avocado.index`
- `dtypes` Nos ayuda ver el tipo de dato de cada columna

`df_books.memory_usage(deep=True)` Checamos la memoria que se esta usando