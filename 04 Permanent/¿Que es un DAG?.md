---
Author: DataCAMP
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-images
  - center-titles
---

# Qué es un DAG


Un [[¿Que es un DAG?]] significa gráfico acíclico dirigido. 

En Airflow, esto representa el conjunto de tareas que componen [[¿Qué es un workflow?|workflow]] 
Consiste en las tareas y las dependencias entre tareas. 

## Propiedades de los Grafos en DAGS

- Está dirigido(Segir una dirección), lo que significa que hay un flujo inherente que representa las dependencias o el orden entre la ejecución de los componentes. 

- Un DAG también es acíclico: no se repite ni se repite. Esto no implica que no se pueda volver a ejecutar todo el DAG, solo que los componentes individuales se ejecutan una vez por ejecución.

![[Pasted image 20240404101453.png]]

## DAG en Airflow


Dentro de Airflow, los DAG están escritos en Python, pero pueden usar componentes escritos en otros lenguajes o tecnologías.
Esto significa que definiremos el DAG usando Python, pero podríamos incluir

- scripts Bash
- Spark

 Los DAG de Airflow se componen de componentes que se ejecutarán como:
- [[¿Qué es un Operator?|Operator]]
- Sensors 
Airflow generalmente se refiere a estos como [[¿Qué son los Task?|Task.]]


>[!tip] Resumen rapido
>Entonces un DAG tiene [[¿Qué son los Task?|Task]] y para hacer las Tareas necesitamos los [[¿Qué es un Operator?|Operators]]
>![[Pasted image 20240404103757.png]]




Los DAG de flujo de aire contienen dependencias que están definidas, ya sea explícita o implícitamente. Estas dependencias definen el orden de ejecución para que Airflow sepa qué componentes deben ejecutarse y en qué punto dentro del flujo de trabajo. 

Ejemplo:
Por ejemplo, es probable que desee copiar un archivo a un servidor antes de intentar importarlo a una base de datos.

## Definir un DAG

Al definir el DAG en Python, primero debe importar el objeto DAG desde el flujo de aire. 

![[Pasted image 20240404102211.png]]

Una vez importado, creamos un diccionario de argumentos predeterminado que consta de atributos que se aplicarán a los componentes de nuestro DAG. 
Estos atributos son opcionales, pero brindan mucho poder para definir el comportamiento en tiempo de ejecución de Airflow. 
![[Pasted image 20240404102328.png]]
Aquí definimos el nombre del propietario como jdoe, una dirección de correo electrónico para cualquier alerta y especificamos la fecha de inicio del DAG. La fecha de inicio representa la fecha y hora más temprana en la que se podría ejecutar un DAG. 

![[Pasted image 20240404102430.png]]

Finalmente, definimos nuestro objeto DAG usando un administrador de contexto de Python, comenzando con DAG, luego el nombre del flujo de trabajo de guión bajo de DAG etl y asignamos el [[directorios]] de argumentos predeterminado al argumento de argumentos de guión bajo predeterminado. Le asignamos el alias `etl_dag`.

Tenga en cuenta que no siempre es necesario utilizar un alias, por lo que es posible que vea DAG de cada tipo.

El resto de nuestro código aparecerá en el bloque del administrador de contexto.

>[!warning] Tenga en cuenta que DAG distingue entre mayúsculas y minúsculas en el código Python.



## DAG en la línea de comando

 El programa de línea de comandos de Airflow contiene muchos subcomandos que manejan varios aspectos de la ejecución de Airflow.  
 ```bash
airflow -h # obtener ayuda y descripciones de los subcomandos. 

airflow dags list #ver todos los DAG reconocidos en una instalación. 
 ```
 
## Línea de comando versus Python

En general, el programa de línea de comandos de Airflow se utiliza para iniciar procesos de Airflow (es decir, servidor web o programador), ejecutar DAG o tareas manualmente y revisar la información de registro. 

El código Python en sí generalmente se usa en la creación y edición de un DAG, sin mencionar el código de procesamiento de datos en sí.