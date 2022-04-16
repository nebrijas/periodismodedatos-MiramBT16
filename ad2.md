# Actividad dirigida 2
En esta actividad hemos realizado un ejercicio de *Web Scraping* sobre la tabla [El medallero de Tokio 2020](https://resultados.elpais.com/deportivos/juegos-olimpicos/medallero/), elaborada por el periódico [El País](https://elpais.com/)

## Objetivo de la actividad
Obtener los resultados obtenidos por los **20 mejores países** participantes en los **Juegos Olímpicos de Tokio 2020**, mediante el análisis previo del código en bruto de la URL de dicha tabla. Para ello es necesario la utilziación de técnicas de *Web Scraping* y el uso de códigos y funciones en lenguaje de *Phyton*

## ¿Cómo lo hemos realizado?
Con la práctica *Scraping* obtenemos de forma automática el contenido de una páginas web a través de su código *HTML*. Gracias al análisis del código en bruto previo, identificamos las principales variables, bucles y acciones a realizar que nos permitirán extraer los datos deseados.  

Para realizar esta técnica son necesarios tres pasos básicos:

1. Elegir la *URL* de la página

2. Estudiar la estructura de la página

3. Obtener los datos y tratarlos

## Código en bruto
En el siguiente apartado encontramos el código utilizado para realizar dicha práctica. También podemos acceder a la explicación de dicho código en sintaxis *Markdown* en el documento [scraping.ipynb](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/scraping.ipynb)

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
