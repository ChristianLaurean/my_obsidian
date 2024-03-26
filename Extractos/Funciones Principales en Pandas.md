---
Author: Platzi
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Curso de Pandas]]"
---
Hay ciertas **_funciones_** que son muy importantes y que siempre estaremos usando a la hora de hacer análisis de datos, para mayor facilidad y comprensión del DataFrame.


```python
df_books.tail()
---> #muestra los ultimos 5 registros
```

- Obtener el **uso de la memoria** de cada columna

```python
df_books.memory_usage(deep=True)
--->
Index            128
Name           59737
Author         39078
User Rating     4400
Reviews         4400
Price           4400
Year            4400
Genre          36440
dtype: int64
```



- **_Eliminar_** registros duplicados

```python
df_books.drop_duplicates()
```
