___

# UT1. A3. Trabajo Con Virtual Hosts.

Esta actividad consiste en configurar 4 sitios web (Virtual Hosts) en nuestro servidor Web Nginx.

---

# Sitio Web 1.

* http://imw.alu5904.me.

Esta página web debe mostrar una página web con la imagen de "Diagrama de unidades de trabajo" de IMW.

Lo primero que hacemos es añadir el fichero de configuración de Nginx que tratará las peticiones que se hagan al nombre de dominio imw.alu5904.me. Para ello vamos a la ruta /etc/nginx/sites-available/ y creamos el fichero imw.

![imagen01](./img/01.png)

Ahora añadimos el contenido a imw.

![imagen02](./img/02.png)

A continuación tenemos que enlazar el fichero que hemos creado para que esté disponible desde los sites-enabled. Para ello entramos a /etc/nginx/sites-enabled, hacemos un enlace simbólico y lo comprobamos.

![imagen03](./img/03.png)

Por último, tenemos que recargar la configuración de Nginx para que los cambios surtan efecto, para ello utilizamos el comando systemctl reload nginx.

![imagen04](./img/04.png)

Ahora tenemos que ir a la moodle de IMW y descargarnos la imagen del Diagrama de unidades de trabajo.

![imagen05](./img/05.png)

![imagen06](./img/06.png)

Ahora la imagen que hemos descargado en la máquina de desarrollo la copiamos a la máquina de producción.

![imagen07](./img/07.png)

Comprobamos que tenemos la imagen en la máquina de producción.

![imagen08](./img/08.png)

Ahora creamos una carpeta que se llame images, cambiamos el nombre de nuestra imagen y la metemos dentro de la carpeta images.

![imagen09](./img/09.png)
![imagen10](./img/10.png)
![imagen11](./img/11.png)

Ahora empezamos a trabajar en el index.html del imw.

![imagen12](./img/12.png)

![imagen13](./img/13.png)

Recargamos la configuración de Nginx para que los cambios surtan efecto.

![imagen14](./img/14.png)

Finalmente entramos desde un navegador a http://imw.alu5904.me.

![imagen15](./img/15.png)

* http://imw.alu5904.me/mec/.

Esta página web debe mostrar una página con un enlace al Real decreto del título de Administración de Sistemas Informáticos en Red - MEC.

Lo primero que hacemos es volver a ir al fichero de configuración de Nginx de imw, es decir, tenemos que ir a la ruta /etc/nginx/sites-available/ y editamos el fichero imw.

![imagen16](./img/16.png)

Ahora añadimos el location a imw del mec.

![imagen17](./img/17.png)

Ahora no tenemos que enlazar el fichero porque ya lo tenemos enlazados anteriormente.

![imagen18](./img/18.png)

Por último, tenemos que recargar la configuración de Nginx para que los cambios surtan efecto, para ello utilizamos el comando systemctl reload nginx.

![imagen19](./img/19.png)

Ahora creamos una carpeta dentro de webapps donde estara el index.html de nuestra página web.

![imagen20](./img/20.png)

Ahora empezamos a trabajar en el index.html del mec.

![imagen21](./img/21.png)

![imagen22](./img/22.png)

Recargamos la configuración de Nginx para que los cambios surtan efecto.

![imagen23](./img/23.png)

Finalmente entramos desde un navegador a http://imw.alu5904.me/mec.

![imagen24](./img/24.png)

Si pinchamos en el enlace se mostrara lo siguiente.

![imagen25](./img/25.png)

___

# Sitio Web 2.

* http://varlib.alu5904.me:9000.

Esta página web debe mostrar el listado de ficheros y directorios de /var/lib de la máquina de producción.

Lo primero que hacemos es añadir el fichero de configuración de Nginx que tratará las peticiones que se hagan al nombre de dominio varlib.alu5904.me:9000. Para ello vamos a la ruta /etc/nginx/sites-available/ y creamos el fichero varlib.

![imagen26](./img/26.png)

Ahora añadimos el contenido a varlib.

![imagen27](./img/27.png)

A continuación tenemos que enlazar el fichero que hemos creado para que esté disponible desde los sites-enabled. Para ello entramos a /etc/nginx/sites-enabled, hacemos un enlace simbólico y lo comprobamos.

![imagen28](./img/28.png)

Por último, tenemos que recargar la configuración de Nginx para que los cambios surtan efecto, para ello utilizamos el comando systemctl reload nginx.

![imagen29](./img/29.png)

Finalmente entramos desde un navegador a http://varlib.alu5904.me:9000.

![imagen30](./img/30.png)

---

# Sitio Web 3.

* https://ssl.alu5904.me/students/.

Esta página web debe mostrar una página web con el nombre de todo el alumnado de clase. Debe pedir usuario/clave. Los datos son: USUARIO: usuario1 y CLAVE: aula108. Debemos prohibir explícitamente el acceso al fichero .htpasswd.

Lo primero que tenemos que hacer es crear una contraseña, para ello utilizamos el comando siguiente, el cual nos cifra la contreña en salt hash.

![imagen31](./img/31.png)

Esta contraseña la introducimos dentro del fichero .htpasswd.

![imagen32](./img/32.png)

Este fichero tendra prohibido el acceso.

![imagen33](./img/33.png)

Luego creamos una carpeta dentro de webapps donde estara el index.html y el .htpasswd de nuestra página web.

![imagen34](./img/34.png)

![imagen35](./img/35.png)

Lo que hacemos ahora es ir al fichero de configuración de Nginx que tratará las peticiones que se hagan al nombre de dominio ssl.alu5904.me/students. Para ello vamos a la ruta /etc/nginx/sites-available/ y editamos el fichero ssl.

![imagen36](./img/36.png)

Ahora añadimos el contenido a ssl.

![imagen37](./img/37.png)

Ahora no tenemos que enlazar el fichero porque ya lo tenemos enlazados anteriormente.

![imagen38](./img/38.png)

Por último, tenemos que recargar la configuración de Nginx para que los cambios surtan efecto, para ello utilizamos el comando systemctl reload nginx.

![imagen39](./img/39.png)

Ahora empezamos a trabajar en el index.html del students.

![imagen40](./img/40.png)

![imagen41](./img/41.png)

Recargamos la configuración de Nginx para que los cambios surtan efecto.

![imagen42](./img/42.png)

Finalmente entramos desde un navegador a http://ssl.alu5904.me/students/.

![imagen43](./img/43.png)

Nos pide un usuario y una contraseña, si la ponemos correcta nos ocurrira lo siguiente.

![imagen44](./img/44.png)

![imagen45](./img/45.png)

En el caso de poner mal la contraseña nos ocurrira lo siguiente.

![imagen46](./img/46.png)

Nos repetira siempre la identificación hasta que pongamos la correcta.

___

# Sitio Web 4.

* http://redirect.alu5904.me.

Esta página web se debe redirigir cualquier petición de este dominio a http://target.alu5904.me.

Lo primero que hacemos es añadir el fichero de configuración de Nginx que tratará las peticiones que se hagan al nombre de dominio imw.alu5904.me. Para ello vamos a la ruta /etc/nginx/sites-available/ y creamos el fichero imw.

![imagen](./img/.png)

Ahora añadimos el contenido a imw.

![imagen](./img/.png)

A continuación tenemos que enlazar el fichero que hemos creado para que esté disponible desde los sites-enabled. Para ello entramos a /etc/nginx/sites-enabled, hacemos un enlace simbólico y lo comprobamos.

![imagen](./img/.png)

Por último, tenemos que recargar la configuración de Nginx para que los cambios surtan efecto, para ello utilizamos el comando systemctl reload nginx.

![imagen](./img/.png)

Ahora empezamos a trabajar en el index.html del redirect.

![imagen](./img/.png)

![imagen](./img/.png)

Recargamos la configuración de Nginx para que los cambios surtan efecto.

![imagen](./img/.png)

Finalmente entramos desde un navegador a http://redirect.alu5904.me, http://www.redirect.alu5904.me/probando y http://www.redirect.alu5904.me/hola.

![imagen](./img/.png)

![imagen](./img/.png)

![imagen](./img/.png)

* http://target.alu5904.me.

Al acceder a esta página web se debe mostrar la página web siguiente initializr-verekia-4.0.zip.

Para copiar y descomprimir el fichero initializr.zip se recomienda usar alguna de las siguientes herramientas: curl, wget, scp, unzip.

Los logfiles deben ser: /var/log/nginx/redirect/access.log y /var/log/nginx/redirect/error.log.

---
