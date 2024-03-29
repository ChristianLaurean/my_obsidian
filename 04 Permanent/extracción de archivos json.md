---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
Para un archivo json podemos hacerlo un DataFrame usando:

```python
df.pd.read_json("file", orient="columns)
```
cuando es una lista de diccionarios la orientación deberia ser records

**parametros**

`index` se pasa para orientar cuando los clave - valor se componen de indices y diccionario que contiene el resto del registro.

cuando hay objetos anidados lo mejor es cargar el archivo a un diccionario con la intención de [[¿Como Crear Un DataFrame?]] lo hacemos con [[Manipular archivos JSON]]
