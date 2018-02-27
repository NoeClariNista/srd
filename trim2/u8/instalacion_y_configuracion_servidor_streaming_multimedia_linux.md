___

# **Instalación Y Configuración De Un Servidor Multimedia (Audio) En Linux.**

---

Vamos a instalar un Servicio de audio orientado a una emisión de radio musical.

Descargamos e instalamos el paquete IceCast (Servidor de Audio) con el comando apt-get install icecast2.

![imagen01](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/01.png)

![imagen02](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/02.png)

Editamos el fichero `/etc/icecast/icecast2.xml` y modificamos las siguientes líneas.

![imagen03](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/03.png)

![imagen04](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/04.png)

Editamos el fichero `/etc/default/icecast2` y modificamos la siguiente línea.

![imagen05](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/05.png)

![imagen06](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/06.png)

Iniciamos el Servicio correspondiente a Icecast con el comando `/etc/init.d/icecast2` start.

![imagen07](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/07.png)

Instalamos el codificador vorbis ices2 con el comando apt-get install ices2.

![imagen08](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/08.png)

Creamos el directorio para el codificador y copiamos el fichero de configuración por defecto.

![imagen09](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/09.png)

Editamos el fichero de configuración del codificador y establecemos los parámetros de nuestra emisora mediante las siguientes etiquetas.

![imagen10](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/10.png)

![imagen11](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/11.png)

![imagen12](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/12.png)

Recopilar unos cuantos ficheros de audio en formato ogg y copiarlos en el directorio `/tmp/música`.

![imagen13](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/13.png)

Generamos la lista de reproducción con el comando find `/tmp/música` –iname `“*.ogg”` > `/etc/icecast2/playlist.txt`.

![imagen14](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/14.png)

Creamos el directorio log de ices2.

![imagen15](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/15.png)

Ejecutamos el codificador en background con el comando $ ices2 `/etc/ices2/ices-playlist.xml` &.

![imagen16](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/16.png)

Procedemos a acceder al entorno web de información y administración de nuestro Servidor de audio Icecast, a través de la IP (o nombre DNS) del Servidor y el puerto configurado anteriormente (8000). Accedemos con el nombre de usuario y contraseña que establecimos en la configuración.

![imagen17](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/17.png)

Comprobamos estado del servicio, configuración y propiedades. Comprobar asimismo punto de montaje (Mountpoint) asociado a la lista de reproducción creada y propiedades.

![imagen18](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/18.png)

Accedemos vía web a la lista de reproducción (mountpoint) desde el propio Servidor (IPServidor:puerto/mountpoint).

![imagen14](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/14.png)

Accedemos desde un posible Cliente (Linux o Windows), a través de un navegador, tanto al entorno de administración como a la reproducción de la lista.

![imagen14](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/14.png)

Tratamos de realizar una reproducción del Streaming de audio creado utilizando un software reproductor multimedia desde el Cliente (URL-> IP:puerto/mountpoint).

![imagen14](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/14.png)

Investigamos en grupos el uso de uno de los siguientes paquetes de streaming de video para Linux.
* Darwin Streaming Server.
* MediaTomb.
* uShare.
* GMediaServer.

---
