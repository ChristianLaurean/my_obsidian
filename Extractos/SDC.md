---
Author: Platzi
Category: Modelado de datos
Type: Apunte
Status: 
relación: "[[Curso Data Warehousing y Modelado OLAP]]"
---
# Dimensiones lentamente cambiantes
Slowly Changing Dimensions

Se refiera a cómo manejar los cambios en los atributos de las dimensiones a lo largo del tiempo.

>[! tip] Tipo 1 SDC
>Los atributos de las dimensiones se sobreescriben con los nuevos valores cuando ocurre un cambio esto significa que no almacena historia y solo refleja valores mas recientes.
>
>Ejem:
>"Tenemos un registro en la base de datos "Producto" asignado a la categoría de jins_Azules si se llegara a cambiar ese atributo solo hay que sobreescribir y listo
>![[Pasted image 20240209090504.png]]
>
Tipo 1 SCD son adecuados cuando la información histórica no es importante o cuando se puede recuperar de otras fuentes.


>[! tip] Tipo 2
> En este tipo, se inserta un nuevo registro en la tabla de dimensiones para representar los valores modificados de los atributos.
>  Por lo general, se utilizan [[Claves sustitutas]] y fechas efectivas para rastrear las diferentes versiones. Los Tipo 2 SCD se utilizan comúnmente cuando se requiere análisis histórico y la dimensión cambia con relativa poca frecuencia.
>ejem
>Ahora cuando cargemos los datos vamos a insertar un nuevo registro a la [[Dimensiones|dimensión]] el Star_date y end_date podemos ver la vigencia.
>![[Pasted image 20240209091539.png]]



>[! tip] Tipo 3
>Este tipo implica agregar columnas a la tabla de dimensiones para almacenar tanto los valores actuales como los valores anteriores de ciertos atributos.
>
Este enfoque permite un seguimiento limitado de los cambios a lo largo del tiempo, pero puede que no capture la historia completa de la dimensión.
>
>Se crea una nueva columna colocando facultad nueva
>![[Pasted image 20240209092636.png]]
>
>Los Tipo 3 SCD se utilizan cuando es importante realizar un seguimiento de cambios específicos de atributos mientras se mantiene la simplicidad en el modelo de datos.

tipo 6 
![[Pasted image 20240209093522.png]]
