# Actividad Dirigida 4

En esta actividad hemos analizado la información de los accidentes de tráfico en la provincia de **Zaragoza**. Para acceder a los datos abiertos hemos instalado la librería `pandas`y la librería `folium` para poder acceder al mapa de la provincia. A través de la [URL]('https://www.zaragoza.es/sede/servicio/transporte/accidentalidad-trafico/accidente.csv?rows=20') de la sede de tráfico de Zaragoza y hemos obtenido los datos de accidentalidad para elaborar los mapas de tráfico.

## ¿Cómo lo hemos realizado?
Para obtener toda los datos e información hemos utilizado una serie de funciones y códigos en lenguaje de programación *Python*. Los pasos seguidos han sido explicados en lenguaje *Markdown* en el documento [**api-pandas-folium2.ipynb**](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-pandas-folium2.ipynb). El código completo también se encuentra en el documento en *html* [**api-pandas-folium2.html**](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-pandas-folium2.html)

Los mapas del territorio aragonés representados contienen marcadores que indican los puntos exactos donde se han producido los accidentes de tráficos,para ello hemos utilizado la función `folium.Marker`.

- Por último hemos representado también el mapa de **Madrid** utilizando las coordenadas *40.4165,-3.70256*, guardado también *html*
