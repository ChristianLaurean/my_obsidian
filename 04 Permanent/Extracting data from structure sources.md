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
Los datos podemos extraer del [[Source]] son:
- [[manipular archivos CSV|CSV]]
- [[Extraccipon de archivos parquet|parquet]]
- [[Manipular archivos JSON|JSON]]
- [[Extraccion de datos| SQL Databases]]
- [[Curso de APis|APis]]
- [[Web scraping]]
- [[Data Lake]]
- [[Data Warehouse]]

---
# importante

- Fomato: Saber en que formato se encuentran mis [[Source]], deben de estar comatibles con mi [[Data Pipelines]]
- Calidad de los datos: Saber como se encuentran los datos para poder saber como limpiar los datos
- Determinar la frecuencia que debo de extraer los datos y actualizarlos
- Accesibilidad: Debemos tener permisos a las fuentes de datos
- Seguridad: Debo asegurarme de que los datos estén protegidos y de que solo las personas autorizadas tengan acceso a ellos.
- Eficiencia: Buscar la menare mas eficiente de Extraer los datos para evitar retrasos o errores.
--- 

# Tener en cuenta que: 

Cuando construimos nuestro pipeline es importante que sea modular.
Separar la lógica en distintas funciones aumenta la legibilidad de una canalización
Separarla con un "extract" "trasformn" y "carga"

