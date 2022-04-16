# PERIODISMO DE DATOS II: HERRAMIENTAS DIGITALES PARA LA VISUALIZACIÓN Y PRESENTACIÓN DE DATOS

¡Hola a todos! Gracias por dedicar un ratito de vuestro tiempo a consultar los trabajos realizados en este repositorio. Me presento, mi nombre es Miriam Barroso Trigueros, soy periodista y estudiante del **Máster de Periodismo Digital y de Datos** de la *Universidad Nebrija*. Este repositorio está dedicado a la asignatura de **Periodismo de Datos II: Herramientas Digitales para la Visualización y Presentación de Datos**, donde hemos realizado distintas actividades dirigidas sobre *Web Scraping* a lo largo de todo el curso. Aquí podréis conocer los pasos que se han seguido en cada trabajo hasta conseguir los resultados essperados.

A lo largo de la asignatura hemos desarrollado cuatro actividades de temáticas diversas, siempre orientadas al **scrapeo de datos** en diferentes web. Cada trabajo explicado a continuación cuenta con dos archivos principales: uno en sintáxis *Markdown* (terminado en **.md**) donde procedemos a explicar cada ejercicio de manera teórica; y otro en lenguaje de programación *Python* con el código bruto completo y celdas explicativas de cada función en *Markdown* (terminado en **.ipynb**). Procedo a explicar cada proyecto:

- La [Actividad Dirigida 1](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/ad1.md) consiste en un comentario crítico sobre un reportaje de periodismo de datos publicado por [El País](https://elpais.com/). El reportaje denominado [Un salón, un bar y una clase: así contagia el coronavirus en el aire
](https://elpais.com/especiales/coronavirus-covid-19/un-salon-un-bar-y-una-clase-asi-contagia-el-coronavirus-en-el-aire/) y realizado por los periodistas **Mariano Zafra** y **Javier Salas**, explica de forma detallada y visual cómo se transmite el coronavirus a través de aerosoles. Este comentario analiza tanto el código en *HTML* utilizado en cada infografía como la estética y los colores utilizados para desarrollar el proyecto, por qué son un acierto o por qué no.
- La [Actividad Dirigida 2](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/ad2.md) consiste en un ejercicio de *Web Scraping* sobre la tabla [El medallero de Tokio 2020](https://resultados.elpais.com/deportivos/juegos-olimpicos/medallero/), elaborada también por el periódico [El País](https://elpais.com/). El objetivo de dicha actividad es extraer a través de su *URL* los resultados obtenidos por los **20 mejores países** participantes en los **Juegos Olímpicos de Tokio 2020**, mediante el análisis previo del código en bruto de la *URL* de dicha tabla. Para ello utilizamos técnicas de *scraping*, códigos y funciones en lenguaje de *Python*. La explicación de dicho código en sintaxis *Markdown* y *python* se encuentra en el documento [scraping.ipynb](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/scraping.ipynb).
- La [Actividad Dirigida 3](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/ad3.md) se compone de un análisis, comparación y representación gráfica de las bases de datos de contagios por COVID-19 de: **España, Colombia e Italia**. Para ello consultamos previamente el repositorio [COVID 19 API](https://covid19api.com/). Desde el repositorio [api-covid19-pandas.ipynb](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-covid19-pandas.ipynb) accedimos a dicha *API* a través de su [*URL*](https://api.covid19api.com/) donde encontramos las tablas de datos en formato *JSON*. Tras la instalación de librerías y el uso de las funciones que ofrece, conectamos con dicha interfaz y conseguimos leer sus datos, crear tablas y representar gráficamente dichos números.
Esta actividad cuenta con varios documentos: en el documento [api-covid19-pandas.ipynb](api-covid19-pandas.ipynb) encontramos el código completo del *scraping* y la explicación de éste en *Markdown*.
En el documento [api-covid19-pandas.html](api-covid19-pandas.html) disponemos del código bruto en *HTML*.
En [api-covid19-pandas-plot.png](api-covid19-pandas-plot.png) del gráfico de líneas de triple comparativa de los países de *España, Colombia e Italia*
Por último disponemos del documento en *csv* en [api-covid19-pandas-plot.csv](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-covid19-pandas-plot.csv)

- Finalmente en la [Actividad Dirigida 4](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/ad4.md) analizamos la información de los accidentes de tráfico en la provincia de **Zaragoza**. Para acceder a los datos abiertos y acceder al mapa de la provincia instalamos varias librerías. A través de la [URL]('https://www.zaragoza.es/sede/servicio/transporte/accidentalidad-trafico/accidente.csv?rows=20') de la sede de tráfico de Zaragoza conseguimos obtener los datos de accidentalidad para elaborar los mapas de tráfico.
Esta actividad cuenta con varios archivos: en el archivo [api-pandas-folium2.ipynb](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-pandas-folium2.ipynb) encontramos el código completo del *scraping* y la explicación de éste en *Markdown*.
En el documento [api-pandas-folium2.html](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-pandas-folium2.html) disponemos del código bruto en *HTML*. Por último disponemos del documento en *csv* en [api-pandas-folium.csv](https://github.com/nebrijas/periodismodedatos-mirambt16/blob/main/api-pandas-folium.csv)
