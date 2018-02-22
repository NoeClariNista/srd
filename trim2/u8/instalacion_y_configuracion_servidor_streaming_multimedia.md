___

# **Instalación Y Configuración De Un Servidor Multimedia – Smooth Streaming.**

---

Descargamos e instalamos IIS Media Services, soporte de Streaming para el Servidor Web IIS. Comprobamos que aparecen, tanto a nivel de Servidor como en los sitios web, las nuevas opciones de Servicios Multimedia.

![imagen00](./images/instalacion_y_configuracion_servidor_streaming_multimedia/00.png)

Descargamos ejemplos de emisiones multimedia codificadas para su emisión en Streaming Windows Media Samples. Descomprimimos sus contenidos en dos carpetas independientes que nos servirán para su publicación en Streaming.

![imagen00](./images/instalacion_y_configuracion_servidor_streaming_multimedia/00.png)

Creamos dos nuevos sitios web asociados a los contenidos multimedia descargados: `bunny.tudominio.ext` y `elephants.tudominio.ext`. Creamos previamente los registros DNS asociados. Los sitios web deben ofrecerse a través de los enlaces descritos y apuntar a las carpetas físicas donde alojamos los contenidos multimedia respectivos.

![imagen00](./images/instalacion_y_configuracion_servidor_streaming_multimedia/00.png)

Descargamos y descomprimimos el Cliente de reproducción SmoothMediaPlayer. Copiamos los ficheros extraídos en las carpetas de los sitios web – Streaming y editamos el fichero SmoothStreamingPlayer.html para adaptarlo a la emisión en Streaming de los contenidos de cada sitio.

Configuramos ambos sitios web para que accedan de forma predeterminada al archivo html anterior.

Comprobamos desde un navegador en el Servidor la reproducción de ambos sitios.

Comprobamos desde un navegador en una máquina Cliente la reproducción de ambos sitios.

En las características de los Servicios Multimedia de uno de los sitios, examinamos la Limitación de Velocidad de Bits. Incluimos un comentario sobre su significado en el informe.

Examinamos también la característica de Presentaciones de Transmisión por Secuencia Suave (Smooth Streaming) para comprobar el punto de acceso a la presentación y sus contenidos (pistas de audio / video).

---

# **Instalación y Configuración de un Servidor Multimedia – Codificación de contenidos propios.**

---

Descargar e instalar Microsoft Expression Encoder, para su correcta ejecución debes instalar la Característica de Experiencia de Escritorio en tu servidor Windows 2012.

Vamos a crear un nuevo sitio web en IIS para la emisión de una presentación multimedia en Streaming pero, en este caso, se van a utilizar contenidos propios. Asi que, en primer lugar debes contar con una serie de archivos de audio y/o video (formatos mp3, wma, avi, etc.).

A continuación creamos el sitios IIS (lo podemos llamar Playlist) que estaría asociado a un registro DNS (playlist.tudominio.ext) y a una carpeta física (por ahora vacía) en cualquier lugar de tu disco duro.

En este momento, vamos a realizar la codificación de los archivos multimedia que hemos elegido para que puedan emitirse en streaming (ten en cuenta que no se aceptan todos los formatos). Para ello utilizaremos la aplicación Mircosoft Expression Encoder.

Al Ejecutar el codificador (Encoder) seleccionaremos la opción Proyecto de Silverlight. Luego añadiremos   los   archivos   que   nos   interesen   y   procederemos   a   codificarlos. Antes ajustaremos el directorio de salida de la codificación a la carpeta donde alojamos el sitio web Playlist.

Ahora estableceremos como archivo predeterminado la página html que se ha creado en la carpeta Playlist como punto de acceso a la presentación en streaming y reiniciaremos el sitio web.

Sólo nos queda comprobar en el servidor y en un cliente la correcta reproducción de nuestro Playlist.

Como segunda parte de la práctica vamos a crear una segunda lista de reproducción de audio/video (Playlist2) haciendo uso de la característica Listas de Reproducción de IIS y sin utilizar Microsoft Expression Encoder.

Para ello debemos crear un nuevo sitio web en IIS, lógicamente asociado a un registro DNS (URL del sitio) y a una carpeta física en disco.

Antes de comenzar a crear la lista se debe modificar la configuración de Listas de Reproducción permitiendo rutas de acceso absolutas o UNC.

Ahora crearemos nuestra lsita de reproducción con el nombre de archivo Playlist2 y agregando archivos multimedia con ubicación de Ruta de acceso física. Nótese que en este punto se puede decidir la capacidad que tendrá el usuario de controlar la reproducción mediante salto y búsquedas. Se debe configurar la playlist para que, en este caso, el usuario no pueda controlar la reproducción de ningún elemento.

Abrir con un editor la lista de reproducción creada (archivo .isx) y examinar características y parámetros de la lista y sus elementos.

Investigación en grupo → Buscar en Internet como reproducir (desde web o aplicación de
escritorio) Listas de Reproducción isx. Si se localiza un reproductor adecuado, comprobar
reproducción y control de la lista desde el servidor y el cliente.

---
