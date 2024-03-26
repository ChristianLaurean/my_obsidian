---
Author: DataCAMP
Category: ETL
Type: Apunte
Status: Terminado
relación: "[[Extraccion de datos]]"
---
Es un formato de un archivo de codigo abierto orientado a columnas diseñado para un almacenamiento y recuperación de campo eficientes son similares a los [[Importación de archivos CSV|csv]] Solo que leer y escribir son mas rápidos.

```python
df = pd.read_parquet("file", engine="fastparquet")
```