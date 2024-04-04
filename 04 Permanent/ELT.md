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
  - pen-black
---
# Extract -> Load -> Transform

![[Pasted image 20240306090630.png]]

---

>[! success] Ventajas del ELT
>- No necesita un sistema informático separado para el proceso de trasformación
>- Podemos volver a ejecutar el proceso sin afectar a los [[Source]]
>- Se usa para [[Straming]]

>[! warning] Desventajas ELT
>- Mas almacenamiento para almacenar las copias de los datos
>- Debemos de tener consideraciones adicionales para cumplir con los estándares de seguridad  [[PII]]



![[Pasted image 20240212101752.png]]

**Hay veces que extraes los datos, se almacenan y se trasforman mediante un [[Stored Procedures]]**