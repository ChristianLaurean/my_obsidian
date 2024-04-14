---
Author: Platzi
Category: Orquestación
Type: Apunte
Status: Terminado
relación: "[[Airflow]]"
cssclasses:
  - page-white
  - center-titles
---

# instalación 

1.  ir a este link [Link para instalar Airflow](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html)
	1. Puedes seguir todo su tutorial o este tutorial
2. Creamos una carpeta donde tendremos todos los archivos de Airflow.
	1. Tener docker corriendo y docker-compose
3. Ejecutamos este comando 
```bash
curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.8.4/docker-compose.yaml'
```
4. Después este comando:
```bash
mkdir -p ./dags ./logs ./plugins ./config
echo -e "AIRFLOW_UID=$(id -u)" > .env
```
5. inicializar una prueba usamos el comando
```bash
docker compose up airflow-init
```
6. Ejecutamos airflow
```bash
docker compose up -d
```

# configuraciones

Las configuraciones se hacen en un archivo que se llama _airflow.cfg_ o mediante [[Variables_entrno]](docker-compose.yaml)

Buscamos las configuraciones en: [configuraciones de airflow](https://airflow.apache.org/docs/apache-airflow/stable/configurations-ref.html)

1. Presionamos ctr +f para buscar la configuración que queremos
![[Pasted image 20240404114050.png]]
2. copeamos la variable de entorno y lo pegamos en el [[Docker-compose]]
![[Pasted image 20240404114340.png]]
