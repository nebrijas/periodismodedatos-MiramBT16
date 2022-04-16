# AD1_Periodismo de Datos II

## Comentario crítico

### Un salón, un bar y una clase: así contagia el coronavirus en el aire

Este reportaje científico, publicado por *El País* y realizado por los periodistas Mariano Zafra y Javier Salas, explica de forma detallada y de manera visual **cómo se transmite el coronavirus a través de aerosoles.**

El motivo de mi elección se debe a la relevancia social y educativa que este proyecto tuvo en un contexto en el que entender cómo se propagaban los aerosoles de este virus estaba aún por determinar. El miedo, la desinformación y las *fake news* se habían apoderado de la población. Este reportaje **permitió a muchos entender de forma clara** y concisa una parte muy importante de **la transmisión y contagio del COVID-19.**

> Los científicos reconocen abiertamente el papel que desempeña en la pandemia del contagio por aerosoles (...) Son partículas inferiores a 100 micras de diámetro que pueden quedar suspendidas en el aire durante horas

Su publicación tuvo una gran relevancia en redes sociales, combatiendo la ignorancia de quiénes especulaban sobre el virus.

> Sin ventilación, los aerosoles quedan en suspensión y se condensan en la sala a medida que pasa el tiempo.

### Diseño
Otro de los motivos por los que considero que es una de las piezas periodísticas más efectivas que he leído, es su diseño por su efectividad y forma de comunicar. Explicar la propagación de los aerosoles de manera simple y sencilla no es una tarea fácil.

El uso de blanco y negro para las personas en las infografías y el naranja para identificar las partículas me parece bastante acertado. Los colores naranjas captan muy bien la atención del usuario en digital, a la vez que facilitan la comprensión de la información que se quiere transmitir y subrayan los aspectos más destacables. El naranja combina la energía del rojo con la felicidad del amarillo y suele asociarse con emociones positivas, por lo que utilizarlo para este reportaje que narra algo tan complicado como la trasmisión del virus y que tanto miedo daba en ese momento, me parece muy correcto.

Por otro lado, a información visual y la coherencia narrativa están muy bien ordenadas en la historia

### HTML
Si analizamos el código utilizado en el reportaje encontramos varias cosas interesantes. En los apartados ‘Reunión social en un salón’ y  ‘Un bar o restaurante’ encontramos dentro del atributo *class*: “img-block-fixed” con el que determinadas imágenes seleccionadas en el reportaje pasan a formar bloques de imágenes fijas en la página facilitando la usabilidad del usuario y favoreciendo el scroll.

En esta parte han decidido utilizar determinadas imágenes de fondo para mostrar un texto breve. El bloque de imagen, generalmente utilizado para portadas, actúa más bien como un encabezado que como imagen. De esta manera, la superposición que han elegido para las imágenes crea un interesante efecto de desplazamiento. Esta opción facilita la legibilidad de los textos a la vez que nos permite entender paso a paso, cómo los aerosoles se expanden y contagian en espacios cerrados como discotecas o bares.

El resto de infografías están insertadas con etiqueta <img> en formatos *.gif* y *.jpg*. 
Por otro lado, el diseño se adapta perfectamente a todo tipo de pantallas y en especial a la de los móviles, donde la mayoría de los lectores han consumido este reportaje. Los bloques de imagen se mantienen fijos en su oposición y se adaptan a la pantalla al igual que el resto de infografías. Con lo que la claridad de la información no pierde relevancia, ni se ve alterada en ningún momento.

Utilizan el atributo “srcset”, lo que permite cargar las imágenes del reportaje de distinto tamaño en responsive y optimizar los tiempos de carga, mejorando la navegación del usuario.

[Enlace artículo](https://elpais.com/especiales/coronavirus-covid-19/un-salon-un-bar-y-una-clase-asi-contagia-el-coronavirus-en-el-aire/)
