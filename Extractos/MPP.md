---
Author: Coderhouse
Category: concepto
Type: Apunte
Status: Terminado
relación: "[[INGENIERÍA DE DATOS]]"
---
Procesamiento Masivo en Paralelo

Es un tipo de procesamiento de los datos  y el poder de procesamiento es dividido en varios nodos y tiene su propa CPU,memoria y almacenamiento.
- Esta compuesto por un nodo lider que se encarga de delegar las tareas y recoletar los resultados.
- Los nodos worker o comput
**Beneficios** 
Si necesitamos mas poder comunicacional solo basta con agregar un nuevo nodo y esto es cuando hablamos de escalabilidad horizontal.

![[Pasted image 20240306105946.png]]
No comparte nada cada nodo tiene su propio disco,cpu etc.

# ciclo basico o Workflow
- EL nodo lider recibe el pedido externo
- Se encarga de subdividir las tareas mas chicas y manejables y enviarlos a los nodos worker
- El nodo worker recibe la tarea y trata de procesarlo 
- El nodo lider esta en costante comunicación con los nodos hijos.
- Se encarga de reunir toda la información y devolverlo al cliente.
![[Pasted image 20240306110051.png]]
