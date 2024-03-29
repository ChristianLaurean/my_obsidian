---
Author: codigofacilito
Category: Programación
Type: Apunte
Status: Terminado
relación: "[[Web scraping]]"
---
- usaremos la libreria [[Request]]
- Libreria Beautifulsoup - Podemos manipular el DOOM(contenido de la pagina web.)
# **_Creando un objeto BeautifulSoup desde HTML_**

La función `bs4.BeautifulSoup()` debe llamarse con una cadena que contiene el HTML que analizará. La función `bs4.BeautifulSoup()` devuelve un objeto BeautifulSoup . 
## importar
```python
import request
from bs4 import BeautifulSoup


headers = {'User-Agent': 'Your User Agent String'}
res = requests.get('https://nostarch.com')
res.raise_for_status()
encoding = response.encoding
return BeautifulSoup(response.text, 'html.parser', from_encoding=encoding)
```

# **_Encontrar un elemento con el método select()_**

Puedes recuperar un elemento de una página web desde un objeto `BeautifulSoup` llamando al método `select()` y pasando una cadena de un _`selector_ CSS` para el elemento que estás buscando. Los selectores son como expresiones regulares: especifican un patrón a buscar; en este caso, en páginas HTML en lugar de cadenas de texto generales.

|**Selector pasado al método select()**|**Coincidirá . . .**|
|---|---|
|sopa.select('div')|Todos los elementos llamados `<div>` |
|sopa.select('#autor')|El elemento con un atributo `id` de autor. |
|sopa.select('.notice') |Todos los elementos que utilizan un atributo de `clase CSS` llamado `notice` |
|sopa.select('div span')|Todos los elementos llamados `<span>` que están dentro de un elemento llamado `<div>` |
|sopa.select('div > span')|Todos los elementos llamados `<span>` que están _directamente_ dentro de un elemento llamado `<div>` , sin ningún otro elemento intermedio |
|sopa.select('entrada[nombre]')|Todos los elementos llamados `<input>` que tienen un atributo de nombre con cualquier valor |
|sopa.select('entrada[tipo="botón"]')|Todos los elementos llamados `<input>` que tienen un atributo llamado tipo con botón de valor |

El método `select()` devolverá una [[Listas|lista]] de objetos `Tag` , que es como `Beautiful Soup` representa un elemento HTML. La lista contendrá un objeto `Tag` por cada coincidencia en el HTML del objeto `BeautifulSoup` . Los valores de etiqueta se pueden pasar a la función str() para mostrar las etiquetas HTML que representan. Los valores de etiqueta también tienen un atributo attrs que muestra todos los atributos HTML de la etiqueta como un diccionario. 

```python
str(elems[0]) # El objeto Etiqueta como cadena.  
'<span id="autor">Al Sweigart</span>'  
elems[0].getText()  
'Al Sweigart'  
elems[0].attrs  
{'id': 'autor'}
```

Llamar a `getText()` en el elemento devuelve el [[strings]] del elemento o [[HTML]] interno. El texto de un elemento es el contenido entre las etiquetas de apertura y cierre: en este caso, 'Al Sweigart' .

Pasar el elemento a `str()` devuelve una cadena con las etiquetas de inicio y cierre y el texto del elemento. Finalmente, attrs nos proporciona un diccionario con el atributo del elemento, 'id' , y el valor del atributo id , 'author' .

select_one()