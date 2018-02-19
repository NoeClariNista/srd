___

# **Instalación Y Configuración De Un Servidor Multimedia – Smooth Streaming.**

---

Descargamos e instalamos IIS Media Services, soporte de Streaming para el Servidor Web IIS. Comprobamos que aparecen, tanto a nivel de Servidor como en los sitios web, las nuevas opciones de Servicios Multimedia.

Descargamos ejemplos de emisiones multimedia codificadas para su emisión en Streaming Windows Media Samples. Descomprimimos sus contenidos en dos carpetas independientes que nos servirán para su publicación en Streaming.

Creamos dos nuevos sitios web asociados a los contenidos multimedia descargados: `bunny.tudominio.ext` y `elephants.tudominio.ext`. Creamos previamente los registros DNS asociados. Los sitios web deben ofrecerse a través de los enlaces descritos y apuntar a las carpetas físicas donde alojamos los contenidos multimedia respectivos.

Descargamos y descomprimimos el Cliente de reproducción SmoothMediaPlayer. Copiamos los ficheros extraídos en las carpetas de los sitios web – Streaming y editamos el fichero SmoothStreamingPlayer.html para adaptarlo a la emisión en Streaming de los contenidos de cada sitio.

Configuramos ambos sitios web para que accedan de forma predeterminada al archivo html anterior.

Comprobamos desde un navegador en el Servidor la reproducción de ambos sitios.

Comprobamos desde un navegador en una máquina Cliente la reproducción de ambos sitios.

En las características de los Servicios Multimedia de uno de los sitios, examinamos la Limitación de Velocidad de Bits. Incluimos un comentario sobre su significado en el informe.

Examinamos también la característica de Presentaciones de Transmisión por Secuencia Suave (Smooth Streaming) para comprobar el punto de acceso a la presentación y sus contenidos (pistas de audio / video).

---
