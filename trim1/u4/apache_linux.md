___

>Trabajo Realizado Por:
>
>* Noelia Hernández Domínguez.
>
>* Omar Hernández Padrón.

---

# **Práctica Servidor Web Apache - Linux.**

---

## **Apache.**

Instalamos Apache con el comando sudo apt-get install apache2.

![imagen01](./images/apache_linux/01.png)

Comprobamos en la carpeta raíz el sitio web `/var/www/`.

![imagen02](./images/apache_linux/02.png)

Comprobamos el acceso a localhost.

![imagen03](./images/apache_linux/03.png)

Añadimos la línea `www.miempresa.com` asociada a la IP del Servidor, que es 172.18.20.41, en `/etc/hosts`.

![imagen04](./images/apache_linux/04.png)

![imagen05](./images/apache_linux/05.png)

Comprobamos el acceso a `www.miempresa.com`.

![imagen06](./images/apache_linux/06.png)

Reiniciamos Apache con el comando sudo /etc/init.d/apache2 restart.

![imagen07](./images/apache_linux/07.png)

Comprobamos que dentro de `/var/log/apache2/` se encuentran error.log y access.log.

![imagen08](./images/apache_linux/08.png)

---

## **PHP.**

Instalamos PHP con el comando sudo apt-get install php.

![imagen09](./images/apache_linux/09.png)

Tenemos que comprobar el acceso a index.php, el cual tiene el siguiente contenido.

![imagen10](./images/apache_linux/10.png)

~~~
<?php phpinfo(); ?>
~~~

![imagen11](./images/apache_linux/11.png)

![imagen12](./images/apache_linux/12.png)

Utilizamos el comando sudo apt-get install libapache2-mod-php para instalar unos modulos de PHP.

![imagen13](./images/apache_linux/13.png)

Vamos al navegador y comprobamos el acceso a localhost y a `www.miempresa.com`.

![imagen14](./images/apache_linux/14.png)

![imagen15](./images/apache_linux/15.png)

---

## **Host Virtuales.**

Creamos Hosts Virtuales en Apache, es decir, asociamos carpetas con sitios web, `empleados.miempresa.com` a `/var/www/empleados`, y establecemos la configuración en `/etc/apache2/sites-available/000-default.conf`.

Lo primero que hacemos es crear la carpeta empleados en `/var/www`.

![imagen16](./images/apache_linux/16.png)

Dentro de esta carpeta añadimos un index.html.

![imagen17](./images/apache_linux/17.png)

![imagen18](./images/apache_linux/18.png)

Ahora tenemos que ir a `/etc/apache2/sites-available/` y editamos 000-default.conf.

![imagen19](./images/apache_linux/19.png)

![imagen20](./images/apache_linux/20.png)

No hace falta crear un enlace simbólico en `/etc/apache2/sites-enabled` ya que esta creado.

![imagen21](./images/apache_linux/21.png)

Añadimos la línea `empleados.miempresa.com` en `/etc/hosts`.

![imagen22](./images/apache_linux/22.png)

![imagen23](./images/apache_linux/23.png)

Comprobamos el acceso a `empleados.miempresa.com`.

![imagen24](./images/apache_linux/24.png)

---

## **Configurar Sitio Web Seguro Pagos.**

Al instalar Apache, se instala también SSL.

Generamos un certificado autofirmado, para ello introducimos los siguientes comandos.

* openssl genrsa -des3 -out apache.key 1024.
* openssl rsa -in apache.key -out apache.pem.
* openssl req -new -key apache.key -out apache.csr.
* openssl x509 -req -days 360 -in apache.csr -signkey apache.key -out apache.crt.

![imagen25](./images/apache_linux/25.png)

Creamos un nuevo Virtual Host a partir del `/etc/apache2/sites-available/000-default.conf`.

![imagen26](./images/apache_linux/26.png)

![imagen27](./images/apache_linux/27.png)

Hacemos un enlace simbólico en `/etc/apache2/sites-enabled`.

![imagen28](./images/apache_linux/28.png)

Reiniciamos el Servicio de Apache.

![imagen29](./images/apache_linux/29.png)

Habilitamos el módulo SSL apache con el comando sudo a2enmod ssl.

![imagen30](./images/apache_linux/30.png)

Añadimos a /etc/hosts `pagos.miempresa.com`.

![imagen31](./images/apache_linux/31.png)

![imagen32](./images/apache_linux/32.png)

Hacemos la carpeta pagos donde estará un index.html.

![imagen33](./images/apache_linux/33.png)

Dentro de esta carpeta editamos el index.html.

![imagen34](./images/apache_linux/34.png)

![imagen35](./images/apache_linux/35.png)

Comprobamos el acceso a `pagos.miempresa.com`.

![imagen36](./images/apache_linux/36.png)

---

## **Acceso A Carpetas Privadas.**

Autenticación mediante .htaccess, para ello creamos una carpeta de claves, por ejemplo, `/var/claves`.

![imagen37](./images/apache_linux/37.png)

Dentro de la carpeta `/var/www/empleados/` añadimos el .htaccess.

![imagen38](./images/apache_linux/38.png)

![imagen39](./images/apache_linux/39.png)

Lanzamos el comando htpasswd -c /var/claves/noelia noelia para

![imagen40](./images/apache_linux/40.png)

Para hacer que el acceso a `empleados.miempresa.com` sea siempre pidiendo contraseña al usuario tenemos que editar `/etc/apache2/sites-available/000-default.conf`.

![imagen41](./images/apache_linux/41.png)

![imagen42](./images/apache_linux/42.png)

Reiniciamos el Servicio de Apache.

![imagen43](./images/apache_linux/43.png)

Comprobamos el acceso a `empleados.miempresa.com`.

![imagen44](./images/apache_linux/44.png)

![imagen45](./images/apache_linux/45.png)

---

## **MySQL.**

Instalamos MySQL con el comando sudo apt-get install mysql-server.

![imagen46](./images/apache_linux/46.png)

![imagen47](./images/apache_linux/47.png)

![imagen48](./images/apache_linux/48.png)

Instalamos el soporte PHP para MySQL con el comando sudo apt-get install php-mysql.

![imagen49](./images/apache_linux/49.png)

---

## **phpMyAdmin.**

Descargamos la última versión (tar.gz) desde phpmyadmin.net.

![imagen50](./images/apache_linux/50.png)

![imagen51](./images/apache_linux/51.png)

Descomprimimos en la subcarpeta de `/var/www`.

![imagen52](./images/apache_linux/52.png)

![imagen53](./images/apache_linux/53.png)

![imagen54](./images/apache_linux/54.png)

Establecemos la configuración en `/etc/apache2/sites-available`.

![imagen55](./images/apache_linux/55.png)

![imagen56](./images/apache_linux/56.png)

![imagen57](./images/apache_linux/57.png)

Creamos un enlace simbólico en `/etc/apache2/sites-enabled`.

![imagen58](./images/apache_linux/58.png)

Habilitamos el módulo SSL apache con el comando sudo a2ensite 000-phpmyadmin.

![imagen59](./images/apache_linux/59.png)

Añadimos la línea `phpmyadmin.miempresa.com` en /etc/hosts.

![imagen60](./images/apache_linux/60.png)

![imagen61](./images/apache_linux/61.png)

Reiniciamos el Servicio de Apache.

![imagen62](./images/apache_linux/62.png)

Comprobamos el acceso a `phpmyadmin.miempresa.com`.

![imagen63](./images/apache_linux/63.png)

![imagen64](./images/apache_linux/64.png)

Introducimos el usuario root con su contraseña.

![imagen65](./images/apache_linux/65.png)

![imagen66](./images/apache_linux/66.png)

---

## **Plataforma Drupal.**

Vamos a `phpmyadmin.miempresa.com`, introducimos el usuario root con su contraseña.

![imagen67](./images/apache_linux/67.png)

Creamos el usuario alumno.

![imagen68](./images/apache_linux/68.png)

![imagen69](./images/apache_linux/69.png)

Le damos todos los privilegios a este usuario.

![imagen70](./images/apache_linux/70.png)

![imagen71](./images/apache_linux/71.png)

Creamos bases de datos llamada alumnos.

![imagen72](./images/apache_linux/72.png)

![imagen73](./images/apache_linux/73.png)

Descargamos Drupal de la plataforma Drupal.

![imagen74](./images/apache_linux/74.png)

Descomprimimos en la carpeta.

![imagen75](./images/apache_linux/75.png)

Movemos la carpeta descomprimida a `/var/www`.

![imagen76](./images/apache_linux/76.png)

Establecemos la configuración en `/etc/apache2/sites-available`.

![imagen77](./images/apache_linux/77.png)

![imagen78](./images/apache_linux/78.png)

Creamos un enlace simbólico en `/etc/apache2/sites-enabled`.

![imagen79](./images/apache_linux/79.png)

Añadimos la línea `drupal.miempresa.com` en `/etc/hosts`.

![imagen80](./images/apache_linux/80.png)

![imagen81](./images/apache_linux/81.png)

Reiniciamos el Servicio de Apache.

![imagen82](./images/apache_linux/82.png)

Habilitamos el módulo SSL Apache con el comando sudo a2ensite 000-drupal.

![imagen83](./images/apache_linux/83.png)

![imagen84](./images/apache_linux/84.png)

Comprobamos el acceso a `drupal.miempresa.com`. Dentro de aqui realizaremos la instalación y la configuración de la plataforma Drupal en la página principal.

![imagen85](./images/apache_linux/85.png)

![imagen86](./images/apache_linux/86.png)

![imagen87](./images/apache_linux/87.png)

---
