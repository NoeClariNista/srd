___

# **Instalación Y Configuración De Un Servidor Multimedia (Audio) En Linux.**

---

Vamos a instalar un Servicio de Audio orientado a una emisión de radio musical.

Descargamos e instalamos el paquete IceCast (Servidor de Audio) con el comando apt-get install icecast2.

![imagen01](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/01.png)

Mientras hacemos la instalación nos pedirá si queremos configurar Icecast2.

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

Recopilamos unos cuantos ficheros de audio en formato ogg y los copiamos en el directorio `/tmp/música`.

![imagen13](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/13.png)

Creamos el fichero `playlist.txt` y le damos permisos.

![imagen14](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/14.png)

Generamos la lista de reproducción con el comando find `/tmp/música` –iname `“*.ogg”` > `/etc/icecast2/playlist.txt`.

![imagen15](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/15.png)

Creamos el directorio log de ices2.

![imagen16](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/16.png)

Reiniciamos el Servicio de Icecast2.

![imagen17](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/17.png)

Procedemos a acceder al entorno web de información y administración de nuestro Servidor de audio Icecast, a través del `localhost` del Servidor y el puerto configurado anteriormente (8000).

![imagen18](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/18.png)

Accedemos con el nombre de usuario y contraseña que establecimos en la configuración.

![imagen19](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/19.png)

Comprobamos estado del Servicio, configuración y propiedades.

![imagen20](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/20.png)

Accedemos vía web a la lista del punto de montaje desde el propio Servidor.

![imagen21](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/21.png)

Ejecutamos el codificador en background con el comando ices2 `/etc/ices2/ices-playlist.xml` &.

![imagen22](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/22.png)

Comprobamos el punto de montaje asociado a la lista de reproducción creada y propiedades.

![imagen23](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/23.png)

![imagen24](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/24.png)

Accedemos desde un posible Cliente Linux, a través de un navegador, a la reproducción de la lista.

![imagen25](./images/instalacion_y_configuracion_servidor_streaming_multimedia_linux/25.png)

---
