---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - page-white
  - center-images
  - center-titles
  - image-borders
---


# Prueba unitaria de una canalización de datos



Además de la validación de puntos de control y las pruebas de un extremo a otro, las pruebas unitarias son una excelente manera de probar el rendimiento de una canalización de datos.

## Validar una canalización de datos con pruebas unitarias


Las pruebas unitarias son códigos que ayudan a probar la funcionalidad de otro código y se usan comúnmente en flujos de trabajo de ingeniería de software. Las pruebas unitarias son la base para la validación del código y los ingenieros de datos pueden utilizarlas para garantizar que los componentes de una canalización de datos funcionen como se espera. 

También se pueden escribir pruebas unitarias para validar los datos producidos por una canalización. 

En un flujo de trabajo típico de canalización de datos, las pruebas unitarias se escribirán y ejecutarán antes de que se complete la validación de un extremo a otro, para validar tanto el código como los datos resultantes.

![[Pasted image 20240403095424.png]]

##  pytest para pruebas unitarias

 Con pytest, las pruebas unitarias se escriben como funciones. Normalmente, los nombres de estas funciones comienzan con "test", lo que permite a pytest analizar y ejecutar pruebas automáticamente dentro de un proyecto. 
 
 ![[Pasted image 20240403095722.png]]
 
 En este ejemplo, definimos una función test_transformed_data. 
 Esta función afirma que el objeto clean_stock_data efectivamente toma el tipo pd.DataFrame. 
 
 Cuando se ejecuta el comando python dash-m pytest, esta prueba se analizará y ejecutará. Si no se generan AssertionErrors, se generará un mensaje de éxito. 
 
![[Pasted image 20240403095905.png]]



##  afirmar y es instancia


Para verificar el tipo de objeto, usaremos la función `isinstance`.

![[Pasted image 20240403100103.png]]

`isinstance()`  toma dos argumentos: un objeto y un tipo de datos. 

Si el objeto coincide con el tipo de datos, la función devuelve `True`. De lo contrario, `isinstance` devolverá `False`.

Aquí, "ETL" se asigna a la variable pipeline_type e isinstance devuelve True cuando se llama, ya que pipeline_type toma el tipo cadena. 

La palabra clave afirmar valida que una expresión booleana sea verdadera y, en caso contrario, genera un error de aserción. 

![[Pasted image 20240403100428.png]]

Aquí validamos que pipeline_type efectivamente toma el valor "ETL". Dado que la declaración se evalúa como Verdadera, no se genera ningún error. 

## Error de afirmación


En este ejemplo, "ETL" se asigna nuevamente a la variable pipeline_type. Esta vez intentamos afirmar que este objeto es un flotador. Como esto es Falso, se genera un AssertionError, como se muestra aquí. Si esta declaración se colocara dentro de una prueba unitaria, la prueba fallaría al ejecutarse.

![[Pasted image 20240403100605.png]]

![[Pasted image 20240403100628.png]]


## Burlarse de los componentes de la canalización de datos con accesorios


Los accesorios de pytest son funciones que permiten compartir datos y objetos de prueba entre varias pruebas. Se pueden utilizar para simplificar la configuración de las pruebas y proporcionar un conjunto común de datos de prueba para múltiples pruebas. 

![[Pasted image 20240403100747.png]]

En este ejemplo, creamos una funcion llamada clean_data, que devuelve un DataFrame limpio. Luego, el dispositivo se pasa a la función test_transformed_data.

![[Pasted image 20240403100906.png]]

Cuando se ejecute, esta prueba unitaria podrá acceder al DataFrame limpio creado y devuelto por el dispositivo clean_data. 

## Pruebas unitarias de DataFrame


Además de probar funciones, también podemos probar datos.

![[Pasted image 20240403101024.png]]

En este ejemplo, probaremos el marco de datos clean_data pasado a la prueba como un dispositivo. 


- Usando el atributo de columnas de puntos, afirmamos que hay cuatro columnas en este DataFrame. 
- Podemos utilizar otras herramientas integradas, como `min`, para afirmar que todos los valores de la columna abierta toman un valor mayor que cero. Esto se puede llevar un paso más allá validando el valor máximo de esta columna con el método `max`.

- La ejecución de pruebas unitarias con datos ayuda a confirmar que los datos siguen las reglas y requisitos comerciales y puede ayudar a detectar problemas de calidad de los datos antes de enviar una canalización a producción.