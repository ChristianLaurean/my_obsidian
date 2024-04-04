---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - page-white
---


# Ejecutar una canalización de datos en producción.



## Patrones de arquitectura de canalización de datos


Existen varias técnicas para ejecutar una canalización de datos en un entorno similar al de producción. 
Uno de los más comunes es ejecutar un script que activa la lógica de extracción, transformación y carga que forma la canalización.tanto las definiciones de funciones como la ejecución de la canalización existen en un solo archivo. 

![[Pasted image 20240403103233.png]]

>[!warning] Si bien esta es una manera fácil de definir y ejecutar una canalización, no siempre es la mejor. 
>Demasiado código en un solo archivo puede causar confusión al depurar o compartir su código.

>[!succees] 
 Una mejor manera de diseñar una canalización implica almacenar las definiciones de funciones en un archivo separado de la lógica de ejecución. Luego, estas funciones se pueden importar y llamar según sea necesario.
 ![[Pasted image 20240403103359.png]]
 
  Las funciones de extracción, transformación y carga se almacenan en el archivo pipeline_utils-dot-py. Cuando son necesarios para la ejecución, se importan y se llaman.  
  
Este patrón de arquitectura ayuda a separar los detalles de ejecución de las definiciones de la lógica de extracción, transformación y carga.

## Ejecutar una canalización de datos de un extremo a otro



 Primero, importaremos el módulo de registro, así como las funciones de extracción, transformación y carga del archivo pipeline_utils-dot-py.
 
  ![[Pasted image 20240403103824.png]]
  
  Una vez configurado el registrador, podemos ejecutar nuestra lógica ETL dentro de un bloque try-except.

  ![[Pasted image 20240403103946.png]]
   
Esto, junto con nuestras declaraciones de registro, crea una solución básica de monitoreo y alertas que permite a un ingeniero de datos rastrear la ejecución de una canalización. 

## Orquestar canales de datos en producción


Al elegir cómo implementar una canalización de datos, los ingenieros de datos buscan la capacidad de ejecutar una canalización automáticamente según una programación, con recursos flexibles disponibles en tiempo de ejecución. Además de esto, es importante que una canalización vuelva a intentarlo en caso de error y alerte cuando se produzca un error. Si bien hemos podido implementar parte de esta lógica utilizando herramientas propias, la mayoría de los ingenieros de datos recurrirán a una herramienta de orquestación, o ETL, para ayudar a ofrecer un proceso de nivel de producción. Las herramientas de orquestación ofrecen funciones adicionales para la ejecución de una canalización, incluida la programación, el escalamiento de recursos y un manejo de errores más sólido. La herramienta de orquestación más utilizada es Apache Airflow. Un poco más del cuarenta por ciento de todos los canales de datos se implementan utilizando esta herramienta. En términos de participación de mercado, Airflow es, con diferencia, la herramienta más popular para crear, implementar y monitorear canales de datos. Además de ser de código abierto, ofrece una amplia gama de funciones y complementos. Fuera de Airflow, también se utilizan herramientas como Prefect y Dagster para la orquestación. A pesar de la amplia gama de características que las herramientas de orquestación de terceros aportan, muchas canalizaciones todavía se crean sin la ayuda de una herramienta de terceros y utilizan soluciones propias o personalizadas. Elegir una herramienta de orquestación es una decisión importante y, si se elige la herramienta adecuada, puede ayudar a acelerar drásticamente el desarrollo del canal.

1. 1 https://open.substack.com/pub/seattledataguy/p/the-state-of-data-engineering-part?r=1po78c&utm_campaign=post&utm_medium=web