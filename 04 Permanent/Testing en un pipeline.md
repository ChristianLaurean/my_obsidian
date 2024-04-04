---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - page-white
  - center-titles
---
# Técnicas para probar y validad un data pipeline

##  Prueba de canalizaciones de datos


Como cualquier otro código, es importante probar una canalización de datos antes de usarla en un entorno de producción. La validación de una canalización no solo garantizará que los datos se extraigan, transformen y carguen correctamente, sino que también ayudará a limitar los esfuerzos de mantenimiento después de la implementación. 

- Tomarse el tiempo para validar una canalización de datos ayuda a identificar y solucionar problemas de calidad de los datos, lo que a su vez mejora la confiabilidad de los datos. 

-  Al crear una canalización de datos, las pruebas pueden resultar difíciles debido a dependencias del sistema fuente o cambios en los datos. Para ayudar a eliminar el misterio del proceso de :
	- pruebas de un extremo a otro como la 
	- validación de "puntos de control"

##  Entornos de prueba y producción.


Los entornos de prueba y producción son herramientas comunes tanto en ingeniería de datos como de software. Al crear una canalización de datos, los entornos de prueba permiten a los ingenieros de datos realizar cambios y trabajar con datos de muestra sin preocuparse por romper una fuente de datos que los consumidores de datos puedan utilizar. En un entorno de prueba, no es necesario que los datos sean de nivel de producción y los desarrolladores son libres de experimentar al crear nuevas soluciones.

![[Pasted image 20240403091835.png]]

## Probar una canalización de un extremo a otro



Las pruebas de un extremo a otro son una de las mejores formas de validar el rendimiento de la canalización de datos. Al probar una canalización de un extremo a otro, los datos de muestra se deben extraer, transformar y cargar en un entorno de prueba, tal como se haría en producción. 

- Esto ayuda a garantizar que una canalización se ejecute en intentos repetidos y permite que un ingeniero de datos valide los datos en los puntos de control a lo largo de la canalización, tanto durante como después de la ejecución. 

- Documentar el rendimiento de un extremo a otro permite que un ingeniero de datos participe en una revisión por pares e incorpore comentarios en el proceso.

- También permite que los datos de prueba estén disponibles para los consumidores de datos, lo que ayuda a validar el acceso y la satisfacción con la solución.

## Validación de los puntos de control de la tubería


A medida que los datos avanzan a través de una canalización, es esencial garantizar que no se pierda información. 

Una de las mejores formas de hacerlo es validando los datos en un "punto de control".

Existe un "punto de control" entre o después de los componentes de una canalización de datos, como entre los componentes de "extracción" y "transformación" de una canalización de datos, o después de que se hayan cargado los datos. 

- Para verificar podemos usar `.shape` Para validar que se extrageron o transformaron los datos correctamente.
- Tambien podemos usar `.head`

## Validación de marcos de datos


Además de estas comprobaciones, también podemos validar que los DataFrames load_data y clean_stock_data sean iguales. 
Para hacer esto, llamamos al método `.equals()`.

```python
df.equals(df_2)
```

Si los dos DataFrames son iguales, se devuelve `True`. De lo contrario, el valor de retorno será `Falso`. Esta es una gran herramienta para garantizar que no se pierdan datos cuando se cargaron en la base de datos de Postgres.

## Ejemplo

```python

raw_tax_data = extract("raw_tax_data.csv")

clean_tax_data = transform(raw_tax_data)

load(clean_tax_data, "clean_tax_data.parquet")

  
# Extact
print(f"Shape of raw_tax_data: {raw_tax_data.shape}")

print(f"Shape of clean_tax_data: {clean_tax_data.shape}")

  
# Trasformn
to_validate = pd.read_parquet("clean_tax_data.parquet")
print(clean_tax_data.head(3))
print(to_validate.head(3))

  
# carga
# Check that the DataFrames are equal
print(to_validate.equals(clean_tax_data))

```