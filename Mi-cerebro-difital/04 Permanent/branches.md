---
Author: You Tube
Category: Entorno
Type: Video
Status: Terminado
relación: "[[GitHub]]"
---

- En la funcion transformar_datos te falto el tipo de return. En este caso son pd.DataFrame y None. Para validar dos tipos de return podes usar algo asi dependiendo tu version de python https://stackoverflow.com/questions/33945261/how-to-specify-multiple-return-types-using-type-hints
- Metiste la E y T adentro de la funcion obtener_datos_ciudades. Seria mas legible que tengas una funcion que solamente extraiga (como es en tu caso extraer_datos_api), luego contatenas todos los JSONs, y luego mandas todo a la T (en tu caso transformar_datos)

  

Cualquier cosa me encontras en el chat de la plataforma!