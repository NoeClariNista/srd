___

>Trabajo Realizado Por:
>
>* Noelia Hernández Domínguez.
>
>* Omar Hernández Padrón.

---

# **Instalación Y Configuración De Un Servidor Multimedia - Smooth Streaming En Windows 2012 Server.**

---

Descargamos e instalamos el IIS Media Services, soporte de Streaming para el Servidor Web IIS.

![imagen001](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/001.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen002](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/002.png)

![imagen003](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/003.png)

![imagen004](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/004.png)

![imagen005](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/005.png)

![imagen006](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/006.png)

![imagen007](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/007.png)

Vamos a Administrador del Servidor.

![imagen008](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/008.png)

Ahora debemos ir Administrador de Internet Information Services (IIS).

![imagen009](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/009.png)

Comprobamos que aparecen, tanto a nivel de Servidor como en los sitios web, las nuevas opciones de Servicios Multimedia.

![imagen010](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/010.png)

![imagen011](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/011.png)

Descargamos ejemplos de emisiones multimedia codificadas para su emisión en Streaming Windows Media Samples.

![imagen012](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/012.png)

Descomprimimos sus contenidos en dos carpetas independientes que nos servirán para su publicación en Streaming.

![imagen013](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/013.png)

Vamos a Administrador del Servidor.

![imagen014](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/014.png)

Ahora debemos ir Administrador de Internet Information Services (IIS).

![imagen015](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/015.png)

Creamos dos nuevos sitios web asociados a los contenidos multimedia descargados: `bunny.miempresa.com` y `elephants.miempresa.com`. Los sitios web deben ofrecerse a través de los enlaces descritos y apuntar a las carpetas físicas donde alojamos los contenidos multimedia respectivos.

![imagen016](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/016.png)

* `elephants.miempresa.com`.

![imagen017](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/017.png)

![imagen018](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/018.png)

![imagen019](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/019.png)

* `bunny.miempresa.com`.

![imagen020](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/020.png)

![imagen021](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/021.png)

![imagen022](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/022.png)

Vamos a Administrador del Servidor.

![imagen023](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/023.png)

Ahora debemos ir a DNS.

![imagen024](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/024.png)

Creamos los registros DNS asociados a los sitios web `bunny.miempresa.com` y `elephants.miempresa.com`.

![imagen025](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/025.png)

* `bunny.miempresa.com`.

![imagen026](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/026.png)

![imagen027](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/027.png)

![imagen028](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/028.png)

* `elephants.miempresa.com`.

![imagen029](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/029.png)

![imagen030](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/030.png)

![imagen031](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/031.png)

Descargamos y descomprimimos el Cliente de reproducción SmoothMediaPlayer. Copiamos los ficheros extraídos en las carpetas de los sitios web – Streaming.

* `bunny.miempresa.com`.

![imagen032](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/032.png)

![imagen033](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/033.png)

![imagen034](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/034.png)

![imagen035](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/035.png)

![imagen036](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/036.png)

* `elephants.miempresa.com`.

![imagen037](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/037.png)

![imagen038](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/038.png)

![imagen039](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/039.png)

![imagen040](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/040.png)

![imagen041](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/041.png)

Editamos el fichero `SmoothStreamingPlayer.html` para adaptarlo a la emisión en Streaming de los contenidos de cada sitio web.

* `elephants.miempresa.com`.

![imagen042](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/042.png)

* `bunny.miempresa.com`.

![imagen043](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/043.png)

Configuramos ambos sitios web para que accedan de forma predeterminada al archivo html anterior.

* `bunny.miempresa.com`.

![imagen044](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/044.png)

* `elephants.miempresa.com`.

![imagen045](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/045.png)

Antes de comprobar desde un navegador la reproducción tenemos que instalar Silverlight.

![imagen046](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/046.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen047](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/047.png)

![imagen048](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/048.png)

![imagen049](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/049.png)

![imagen050](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/050.png)

Comprobamos desde un navegador en el Servidor la reproducción de ambos sitios.

* `elephants.miempresa.com`.

![imagen051](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/051.png)

* `bunny.miempresa.com`.

![imagen052](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/052.png)

Antes de comprobar desde un navegador la reproducción tenemos que instalar Silverlight.

![imagen053](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/053.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen054](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/054.png)

![imagen055](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/055.png)

![imagen056](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/056.png)

![imagen057](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/057.png)

Comprobamos desde un navegador en una máquina Cliente la reproducción de ambos sitios.

* `bunny.miempresa.com`.

![imagen058](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/058.png)

* `elephants.miempresa.com`.

![imagen059](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/059.png)

En las características de los Servicios Multimedia de uno de los sitios, examinamos la Limitación de Velocidad de Bits.

![imagen060](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/060.png)

![imagen061](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/061.png)

Examinamos también la característica de Presentaciones de Transmisión por Secuencia Suave (Smooth Streaming) para comprobar el punto de acceso a la presentación y sus contenidos (pistas de audio / video).

![imagen062](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/062.png)

![imagen063](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/063.png)

---

# **Instalación Y Configuración De Un Servidor Multimedia - Codificación De Contenidos Propios En Windows 2012 Server.**

---

Descargamos e instalamos Microsoft Expression Encoder.

![imagen064](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/064.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen065](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/065.png)

![imagen066](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/066.png)

![imagen067](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/067.png)

![imagen068](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/068.png)

![imagen069](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/069.png)

![imagen070](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/070.png)

Para su correcta ejecución debemos instalar la Característica de Experiencia de Escritorio en mi Servidor Windows 2012.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen071](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/071.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen072](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/072.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen073](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/073.png)

![imagen074](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/074.png)

![imagen075](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/075.png)

![imagen076](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/076.png)

![imagen077](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/077.png)

![imagen078](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/078.png)

![imagen079](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/079.png)

![imagen080](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/080.png)

Finalmente terminamos la instalación de la Característica de Experiencia de Escritorio en mi Servidor Windows 2012.

![imagen081](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/081.png)

Reiniciamos la máquina virtual para completar la instalación de la característica anteriormente instalada.

![imagen082](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/082.png)

Vamos a crear un nuevo sitio web en IIS para la emisión de una presentación multimedia en Streaming pero, en este caso, se van a utilizar contenidos propios. Así que, en primer lugar debemos contar con una serie de archivos de audio y/o video (formatos mp3, wma, avi).

A continuación creamos el sitios IIS (lo podemos llamar Playlist) que estaría asociado a un registro DNS (playlist.tudominio.ext) y a una carpeta física (por ahora vacía) en cualquier lugar de nuestro disco duro.

* Carpeta física.

![imagen083](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/083.png)

![imagen084](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/084.png)

* Sitios IIS.

![imagen085](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/085.png)

![imagen086](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/086.png)

![imagen087](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/087.png)

![imagen088](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/088.png)

![imagen089](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/089.png)

![imagen090](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/090.png)

* DNS.

![imagen091](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/091.png)

![imagen092](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/092.png)

![imagen093](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/093.png)

![imagen094](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/094.png)

![imagen095](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/095.png)

![imagen096](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/096.png)

En este momento, vamos a realizar la codificación de los archivos multimedia que hemos elegido para que puedan emitirse en streaming. Para ello utilizaremos la aplicación Mircosoft Expression Encoder.

Al Ejecutar el codificador (Encoder) seleccionaremos la opción Proyecto de Silverlight. Luego añadiremos los archivos que nos interesen y procederemos a codificarlos. Antes ajustaremos el directorio de salida de la codificación a la carpeta donde alojamos el sitio web Playlist.

![imagen097](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/097.png)

![imagen098](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/098.png)

![imagen099](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/099.png)

![imagen100](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/100.png)

Ahora estableceremos como archivo predeterminado la página html que se ha creado en la carpeta Playlist como punto de acceso a la presentación en streaming y reiniciaremos el sitio web.

![imagen101](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/101.png)

Sólo nos queda comprobar en el servidor y en un cliente la correcta reproducción de nuestro Playlist.

![imagen102](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/102.png)

![imagen103](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/103.png)

![imagen104](./images/instalacion_y_configuracion_servidor_streaming_multimedia_windows/104.png)

---
