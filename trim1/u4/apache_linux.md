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

Comprobamos en la carpeta raíz el sitio web /var/www.

![imagen02](./images/apache_linux/02.png)

Comprobamos el acceso a localhost.

![imagen03](./images/apache_linux/03.png)

Añadimos la línea `www.miempresa.com` asociada a la IP del Servidor, que es 172.18.20.41, en `/etc/hosts`.

![imagen04](./images/apache_linux/04.png)

![imagen05](./images/apache_linux/05.png)

Comprobamos el acceso a `www.miempresa.com`.

![imagen06](./images/apache_linux/06.png)

Reiniciamos apache con el comando sudo /etc/init.d/apache2 restart.

![imagen07](./images/apache_linux/07.png)

Comrpobamos que dentro de `/var/log/apache2/` se encuentran error.log y access.log.

![imagen08](./images/apache_linux/08.png)

---

## **PHP.**

Instalamos php con el comando sudo apt-get install php.

![imagen09](./images/apache_linux/09.png)

Tenemos que comprobar el acceso a index.php, el cual tiene el siguiente contenido.

![imagen10](./images/apache_linux/10.png)

~~~
<?php phpinfo(); ?>
~~~

![imagen11](./images/apache_linux/11.png)

![imagen12](./images/apache_linux/12.png)

Utilizamos el comando sudo apt-get install libapache2-mod-php para instalar unos modulos de php.

![imagen13](./images/apache_linux/13.png)

Vamos al navegador y comprobamos el acceso a localhost y a `www.miempresa.com`.

![imagen14](./images/apache_linux/14.png)

![imagen15](./images/apache_linux/15.png)

Creamos Hosts Virtuales en Apache, es decir, asociamos carpetas con sitios web, empleados.miempresa.com a /var/www/empleados, y establecemos la configuración en /etc/apache2/sites-available/000-default.conf.

Lo primero es hacer la carpeta en `/var/www`.

![imagen16](./images/apache_linux/16.png)

Ahora tenemos que ir a `/etc/apache2/sites-available/000-default.conf`

![imagen17](./images/apache_linux/17.png)

![imagen18](./images/apache_linux/18.png)

No hace falta crear un enlace simbólico en `/etc/apache2/sites-enabled` ya que esta creado.

![imagen19](./images/apache_linux/19.png)

---

## **Configurar Sitio Web Seguro Pagos.**

Al instalar Apache, se instala también SSL.

Generamos certificado autofirmado:

* openssl genrsa -des3 -out server.key 1024
* openssl rsa -in server.key -out server.pem
* openssl req -new -key server.key -out server.csr
* openssl x509 -req -days 360 -in server.csr -signkey server.key -out server.crt

![imagen20](./images/apache_linux/20.png)

Creamos un nuevo virtual host a partir del /etc/apache2/sites-available/000-default.conf según indicaciones PDF para crear host virtual seguro

![imagen21](./images/apache_linux/21.png)

![imagen22](./images/apache_linux/22.png)

Hacemos un enlace simbólico en `/etc/apache2/sites-enabled`

![imagen23](./images/apache_linux/23.png)

Habilitamos el módulo SSL apache con el comando sudo a2enmod ssl.

![imagen24](./images/apache_linux/24.png)

![imagen25](./images/apache_linux/25.png)

Añadimos a /etc/hosts pagos.miempresa.com.

![imagen26](./images/apache_linux/26.png)

![imagen27](./images/apache_linux/27.png)

Hacemos la carpeta pagos donde estará un index.html.

![imagen28](./images/apache_linux/28.png)

---

## **Acceso A Carpetas Privadas.**

Autenticación mediante .htaccess.

![imagen29](./images/apache_linux/29.png)

![imagen30](./images/apache_linux/30.png)

![imagen31](./images/apache_linux/31.png)

![imagen32](./images/apache_linux/32.png)

Estructura: empleados.miempresa.com (acceso a todos los empleados pero no anónimos) y subcarpetas personales de empleados (dos o tres, con acceso limitado al usuario)

![imagen33](./images/apache_linux/33.png)

![imagen34](./images/apache_linux/34.png)

![imagen35](./images/apache_linux/35.png)

![imagen36](./images/apache_linux/36.png)

![imagen37](./images/apache_linux/37.png)

---

## **MySQL.**

Instalar MySQL: sudo apt-get install mysql-server.

![imagen38](./images/apache_linux/38.png)

![imagen39](./images/apache_linux/39.png)

![imagen40](./images/apache_linux/40.png)

Instalar soporte php para MySQL: sudo apt-get install php-mysql.

![imagen41](./images/apache_linux/41.png)

---

## **phpMyAdmin.**

Descargar última versión (tar.gz) desde phpmyadmin.net, descomprimir en subcarpeta de /var/www (u otra asociada por host virtual) y comprobar acceso.

![imagen42](./images/apache_linux/42.png)

![imagen43](./images/apache_linux/43.png)

![imagen44](./images/apache_linux/44.png)

![imagen45](./images/apache_linux/45.png)

![imagen46](./images/apache_linux/46.png)

![imagen47](./images/apache_linux/47.png) <- arreglar

![imagen48](./images/apache_linux/48.png) <- arreglar

![imagen49](./images/apache_linux/49.png)

![imagen50](./images/apache_linux/50.png)

![imagen51](./images/apache_linux/51.png)

![imagen52](./images/apache_linux/52.png)

![imagen53](./images/apache_linux/53.png)

![imagen54](./images/apache_linux/54.png)

![imagen55](./images/apache_linux/55.png)

![imagen56](./images/apache_linux/56.png)

![imagen57](./images/apache_linux/57.png)

![imagen58](./images/apache_linux/58.png)

---

## **Plataforma Drupal / Joomla / Moodle / etc.**

Creación bases de datos y usuarios necesarios.

![imagen59](./images/apache_linux/59.png)

![imagen60](./images/apache_linux/60.png)

![imagen61](./images/apache_linux/61.png)

![imagen62](./images/apache_linux/62.png)

![imagen63](./images/apache_linux/63.png)

![imagen64](./images/apache_linux/64.png)

![imagen65](./images/apache_linux/65.png)

Descargamos, hacemos la instalación y la configuración de la plataforma Drupal en la página principal.

![imagen66](./images/apache_linux/66.png)

![imagen67](./images/apache_linux/67.png)

![imagen68](./images/apache_linux/68.png) <- arreglar

![imagen69](./images/apache_linux/69.png) <- arreglar

![imagen70](./images/apache_linux/70.png)

![imagen71](./images/apache_linux/71.png) <- arreglar

![imagen72](./images/apache_linux/72.png) <- arreglar

![imagen73](./images/apache_linux/73.png)

![imagen74](./images/apache_linux/74.png) <- arreglar

![imagen75](./images/apache_linux/75.png) <- arreglar

![imagen76](./images/apache_linux/76.png)

![imagen77](./images/apache_linux/77.png)

![imagen78](./images/apache_linux/78.png)

![imagen79](./images/apache_linux/79.png)

---
