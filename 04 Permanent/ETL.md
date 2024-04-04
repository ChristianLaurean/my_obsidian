---
Author: DataCAMP
Category: Pipelines
Type: Apunte
Status: Terminado
relación: "[[Data Pipelines]]"
cssclasses:
  - center-images
  - center-titles
  - page-white
---
# Extract - Transform - Load

![[Pasted image 20240306084740.png]]

**Extraer**: Extraer los datos de una fuente

**Trasformación**: trasformamos los datos a las necesidades de nuestro proyecto.

**Load**: Cargarlos en un repositorio unificado y enriquecido.

Ventajas

>[! success] Ventajas del ETL
>- Almacenamos datos limpios
>- Costos de almacenamiento mas bajos por que solo guarda copias de los datos trasformados y limpios
>- Podemos detectar anomalías en el [[Source]]
>- Cumple con estándares de seguridad evitamos datos [[PII]] Con esto evitamos almacenar datos delicados al [[Data Warehouse]]


>[! warning] Desventajas del ETL
>- No almacenamos los datos originales

## Extract

- Es extraer los datos de los sistemas de [[Source|origen]]

### Transform

- trasformamos los datos dependiendo las reglas de negocio
- [[Data clean]]

## Load
- Carga los datos en una base de datos

![[Pasted image 20240212101718.png]]
