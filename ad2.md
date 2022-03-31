# Actividad dirigida 2
## Práctica de Web Scraping paso a paso
Con la práctica *Scraping* obtenemos de forma automática el contenido de una páginas web a través de su código HTML

## Pasos
Para realizar esta técnica son necesarios tres pasos básicos

**1. Elegir la URL de la página**

**2. Estudiar la estructura de la página**

**3. Obtener los datos y tratarlos**

### Elegir la URL de la página
Para ello primero será necesario interactuar con la URL elegida a través de librerías que nos permitan cargar páginas web. Estas son `requests`y `BeautifulSoup`

### Importamos estas librerías
Con la librería [requests](https://docs.python-requests.org/en/latest/) descargamos el contenido de la página El contenido de la respuesta, el que contiene la página en HTML, será el que pasemos posteriormente a `BeautifulSoup`para generar el árbol de elementos y poder hacer consultas al mismo.

Después importamos la librería [bs4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) `BeautifulSoup` El contenido de la página obtenido en el paso anterior será el que utilicemos para crear la «sopa», esto es, el árbol de objetos *Python* que representan al documento *HTML*.

Para ello, hay que crear un objeto de tipo `BeautifulSoup`, al cual pasamos el texto en formato *HTML* y el identificador del *parser* a utilizar

### Definimos URL
En este caso la URL pertenece a el periódico El País = "https://resultados.elpais.com/deportivos/juegos-olimpicos/medallero/"

Es importante que comprobemos primero que podemos acceder a estos datos, para ello primero preguntamos hacemos la consulta. Si los accesos nos devuelven `HTTP 200 Ok`, la respuesta es correcta. Si no, lanzamos la excepción de que no podemos acceder.

 ### Realizamos la petición a la web
 Si el estatus code no es `200` no se puede leer la página

 ### De requests a Beautiful Soupe

 Como hemos mencionado antes tenemos que crear un objeto de tipo `BeautifulSoup()` al cual pasamos el texto en formato *HTML* y el identificador del parser a utilizar

 ###  Variables de datos
 Es necesario estudiar la estructura *HTML* de la página para poder obtener los datos, que es el objetivo del *Web Scraping*. Para ello debemos conocer la estructura de la página y una vez conocida, a través de la librería de `BeautifulSoup` podremos ir obteniendo las diferentes estructuras HTML que hay en ellas y recolectando los datos.

 Definimos las variables `paises`, `oros`, etc y las identificamos con la función `find_all()`

 Como se puede observar, con `find_all` obtendremos los trozos de código necesario para obtener los datos. Con estas funciones podemos ir obteniendo los elementos que nos interesan para obtener los datos que tienen y poder tratarlos.

### Hacemos la pregunta

### Bucle para obtener los datos
Creamos un bucle con `for`y `else`

# Código en bruto

```
from bs4 import BeautifulSoup
import requests
#Datos sobre los Juegos Olímpicos en 2020

respuesta=input('¿QUIERES CONOCER LOS 20 PAÍSES QUE HAN OBTENIDO MÁS MEDALLAS EN 2020?\n \n Si tu respuesta es Sí, presiona "s" \n')
if(respuesta == 's'):
  print('\nRESULTADOS DE LOS DATOS DE LOS JUEGOS OLÍMPICOS 2020\n')
  print ('PAÍSES')
  URL = "https://resultados.elpais.com/deportivos/juegos-olimpicos/medallero/"
  # Realizamos la petición a la web
  req = requests.get(URL)
  # Si el estatus code no es 200 no se puede leer la página
  if (req.status_code != 200):
    raise Exception("No se puede hacer Web Scraping en"+ URL)
  # Pasamos el contenido HTML de la web a un objeto BeautifulSoup()
  html = BeautifulSoup(req.text, "html.parser")
  # Obtenemos todos los divs donde están las entradas
  paises = html.find_all("th",{"class":"pais"})
  oros = html.find_all("td",{"class":"m_oro"})
  platas = html.find_all("td",{"class":"m_plata"})
  bronces = html.find_all("td",{"class":"m_bronce"})
  totales = html.find_all("td",{"class":"m_total"})
  for i in range (20):
    # Con el método "getText()" no nos devuelve el HTML
    print("%d. %s \nOro: %s Plata: %s Bronce: %s \n Total: %s \n " % (i+1, paises[i+1].text.strip(),oros[i].text.strip(),platas[i].text.strip(),bronces[i].text.strip(), totales[i].text.strip()))

else:
  print('Qué lástima, y...')
```
