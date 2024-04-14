---
Author: You Tube
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-titles
---
# ¿Como instalar librerías o paquetes?

- Con [[Dockerfiles]]
- Creamos un Requirements.txt
	- installamos las credenciales
![[Pasted image 20240413120320.png]]
- actualizamos la imgen: -extending_airflow:latest202404![[Pasted image 20240413124246.png]]
- colocamos esto en la terminal
- ![[Pasted image 20240413120552.png]]
- volvemos a ejecutar docker  compose
	- ![[Pasted image 20240413120915.png]]

#### Entrar al airflow



# Test con airflow
- Entramos a airflow con docker
```bash
docker exec -it cod_cont bash
```
- Despues
```bash
airflow tasks test nombre_dag nombre_tarea_id fecha
```
## iniciando con airflow
```python

```
