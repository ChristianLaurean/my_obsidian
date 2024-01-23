---
Author: Coderhouse
Category: Fundamentos de Data
Type: Apunte
Status: Terminado
relación: "[[fundamentos de Ingenieria de datos]]"
---
# Online Analytical processing

Se encargan en la lectura de datos a gran escala para consultar analitycas.

Preguntas que se hacen
- Promedio
- Cantidad de dinero que se gano por trimestre 
- La suma de todo el balance por cliente

> Son usadas por analitas y data science y buscan información valiosa de los datos. 

Se usan mucho los [[SELECT]] sobre gran cantidad de datos.
Los [[INSERT]] se suelen hacer Masiva mente por periodos de tiempo que sea necesario para el negocio y se usan procesos de [[ETL]] para cargar los datos a la [[Base de datos]] tipo [[OLAP]]

>[!succes] Los datos se encuentras [[de-normalizados]]
Es importante guardar su historia.
