___

>Trabajo Realizado Por:
>
>* Noelia Hernández Domínguez.
>
>* Omar Hernández Padrón.

---

# **Servidor Web Avanzado 2.**

---

## **Instalación De PHP, MySQL Y PHPMyAdmin.**

Vamos a realizar las instalaciones y configuraciones necesarias para obtener un Servidor Web con soporte PHP y accesos a bases de datos relacionales, acceso FTP y gestor de bases de datos. Sobre este Servidor, podremos realizar instalaciones de aplicaciones integradas (CMS, e-commerce, etc) desde el propio Servidor o en modo remoto desde un Cliente W10.

Lo primero que tenemos que hacer es ir a panel de Administración de Servidor y vamos a agregar roles/características y agregamos el rol de CGI, con esto nos descargamos IIS Fast CGI.

![imagen01](./images/servidor_web_avanzado_2/01.png)

![imagen02](./images/servidor_web_avanzado_2/02.png)

Instalamos el soporte para PHP para tus sitios Web gestionados por IIS. Se recomienda PHP-5.3.9-nts-Win32-VC9-x86.msi. Nos descargarmos la versión de PHP, para ello vamos a la página de [PHP](windows.php.net/downloads/releases/archives).

Los pasos los realizamos como se pueden ver en las imágenes.

![imagen03](./images/servidor_web_avanzado_2/03.png)

![imagen04](./images/servidor_web_avanzado_2/04.png)

![imagen05](./images/servidor_web_avanzado_2/05.png)

![imagen06](./images/servidor_web_avanzado_2/06.png)

![imagen07](./images/servidor_web_avanzado_2/07.png)

![imagen08](./images/servidor_web_avanzado_2/08.png)

Comprobamos la instalación correcta de PHP colocando un fichero index.php en el sitio web destinado a gestionar el CMS Drupal (www.miEmpresa.com) con el siguiente código: `<?php phpinfo(); ?>`

![imagen09](./images/servidor_web_avanzado_2/09.png)

![imagen10](./images/servidor_web_avanzado_2/10.png)

![imagen11](./images/servidor_web_avanzado_2/11.png)

Instalamos el Servidor de bases de datos relacionales MySQL para tus sitios Web gestionados por IIS. Descargar para ello el paquete instalador de http://dev.mysql.com/downloads/installer/. Instalamos MySQL y complementos necesarios.

Los pasos los realizamos como se pueden ver en las imágenes.

![imagen12](./images/servidor_web_avanzado_2/12.png)

![imagen13](./images/servidor_web_avanzado_2/13.png)

![imagen14](./images/servidor_web_avanzado_2/14.png)

Descargamos e instalamos .NET Framework 4.0.

![imagen15](./images/servidor_web_avanzado_2/15.png)

![imagen16](./images/servidor_web_avanzado_2/16.png)

Los pasos los realizamos como se pueden ver en las imágenes.

![imagen17](./images/servidor_web_avanzado_2/17.png)

![imagen18](./images/servidor_web_avanzado_2/18.png)

![imagen19](./images/servidor_web_avanzado_2/19.png)

![imagen20](./images/servidor_web_avanzado_2/20.png)

![imagen21](./images/servidor_web_avanzado_2/21.png)

![imagen22](./images/servidor_web_avanzado_2/22.png)

![imagen23](./images/servidor_web_avanzado_2/23.png)

![imagen24](./images/servidor_web_avanzado_2/24.png)

![imagen25](./images/servidor_web_avanzado_2/25.png)

![imagen26](./images/servidor_web_avanzado_2/26.png)

![imagen27](./images/servidor_web_avanzado_2/27.png)

![imagen28](./images/servidor_web_avanzado_2/28.png)

![imagen29](./images/servidor_web_avanzado_2/29.png)

![imagen30](./images/servidor_web_avanzado_2/30.png)

![imagen31](./images/servidor_web_avanzado_2/31.png)

Instalamos PHPMyAdmin para tus sitios Web gestionados por IIS. Para esto debes crear un nuevo sitio web asociado a phpmyadmin.miEmpresa.com, recordando crear la correspondiente carpeta (donde descomprimirás los ficheros de phpMyAdmin) y actualizar DNS.

![imagen32](./images/servidor_web_avanzado_2/32.png)

![imagen33](./images/servidor_web_avanzado_2/33.png)

![imagen34](./images/servidor_web_avanzado_2/34.png)

![imagen35](./images/servidor_web_avanzado_2/35.png)

![imagen36](./images/servidor_web_avanzado_2/36.png)

![imagen37](./images/servidor_web_avanzado_2/37.png)

![imagen38](./images/servidor_web_avanzado_2/38.png)

![imagen39](./images/servidor_web_avanzado_2/39.png)

---

## **Instalación De Servidor FTP Y CMS Drupal.**

Instalamos Servidor FTP FileZilla en Windows 2012 Server. Nos descargamos Filezilla en desde la página de [Filezilla](http://filezilla-project.org/download.php?type=server).

![imagen40](./images/servidor_web_avanzado_2/40.png)

![imagen41](./images/servidor_web_avanzado_2/41.png)

![imagen42](./images/servidor_web_avanzado_2/42.png)

![imagen43](./images/servidor_web_avanzado_2/43.png)

![imagen44](./images/servidor_web_avanzado_2/44.png)

![imagen45](./images/servidor_web_avanzado_2/45.png)

![imagen46](./images/servidor_web_avanzado_2/46.png)

Creamos un usuario denominado `ftpuser` en el Servidor FTP y le asociamos a este usuario permisos de Control Total sobre la carpeta en la que se va a instalar el CMS de miEmpresa.

![imagen47](./images/servidor_web_avanzado_2/47.png)

![imagen48](./images/servidor_web_avanzado_2/48.png)

![imagen49](./images/servidor_web_avanzado_2/49.png)

Creamos un nuevo registro DNS que nos permita acceder a nuestro sitio FTP a través de la dirección `ftp.miEmpresa.com`.

![imagen50](./images/servidor_web_avanzado_2/50.png)

![imagen51](./images/servidor_web_avanzado_2/51.png)

Comprobamos el acceso al sitio FTP a través de un navegador desde localhost y a tráves de la dirección `ftp.miEmpresa.com`, todo esto conectandonos con el usuario que hemos creado anteriormente.

![imagen52](./images/servidor_web_avanzado_2/52.png)

![imagen53](./images/servidor_web_avanzado_2/53.png)

![imagen54](./images/servidor_web_avanzado_2/54.png)

![imagen55](./images/servidor_web_avanzado_2/55.png)

A partir de ahora realizaremos todo desde el cliente Windows 10.

Comprobamos el acceso a phpMyAdmin desde un navegador (phpmyadmin.miEmpresa.com).

![imagen56](./images/servidor_web_avanzado_2/56.png)

![imagen57](./images/servidor_web_avanzado_2/57.png)

![imagen58](./images/servidor_web_avanzado_2/58.png)

Descargamos CMS Drupal de drupal.org. Nos descargamos Drupal desde la página de [Drupal](http://drupal.org/project/drupal)

Comprobamos el acceso al sitio FTP creado a través de un navegador y con el usuario ftpuser. Antes de comprobarlo tenemos que añadir unas reglas de entrada y de salida al Firewall para que nos permita conectar el Cliente con el Servidor.

![imagen59](./images/servidor_web_avanzado_2/59.png)

![imagen60](./images/servidor_web_avanzado_2/60.png)

![imagen61](./images/servidor_web_avanzado_2/61.png)

![imagen62](./images/servidor_web_avanzado_2/62.png)

![imagen63](./images/servidor_web_avanzado_2/63.png)

![imagen64](./images/servidor_web_avanzado_2/64.png)

![imagen65](./images/servidor_web_avanzado_2/65.png)

![imagen66](./images/servidor_web_avanzado_2/66.png)

Intentamos acceder a tráves de un navegador y con el usuario ftpuser.

![imagen67](./images/servidor_web_avanzado_2/67.png)

![imagen68](./images/servidor_web_avanzado_2/68.png)

Instalamos un Cliente FTP (p.e.: FileZilla) en Windows 10 para poder realizar todas las operaciones sobre los ficheros y carpetas del servidor web. Nos descargamos Filezilla en la página de [Filezilla](http://filezilla-project.org/download.php?type=client).

![imagen69](./images/servidor_web_avanzado_2/69.png)

![imagen70](./images/servidor_web_avanzado_2/70.png)

![imagen71](./images/servidor_web_avanzado_2/71.png)

![imagen72](./images/servidor_web_avanzado_2/72.png)

![imagen73](./images/servidor_web_avanzado_2/73.png)

Descomprimir y subir archivos Drupal a carpeta principal (www.miEmpresa.com).

![imagen74](./images/servidor_web_avanzado_2/74.png)

![imagen75](./images/servidor_web_avanzado_2/75.png)

![imagen76](./images/servidor_web_avanzado_2/76.png)

![imagen77](./images/servidor_web_avanzado_2/77.png)

Crear una nueva base de datos, denominada cms, a través de phpMyAdmin.

![imagen78](./images/servidor_web_avanzado_2/78.png)

![imagen79](./images/servidor_web_avanzado_2/79.png)

![imagen80](./images/servidor_web_avanzado_2/80.png)

![imagen81](./images/servidor_web_avanzado_2/81.png)

Crear usuario cms y asignar todos los privilegios para la base de datos anterior.

![imagen82](./images/servidor_web_avanzado_2/82.png)

![imagen83](./images/servidor_web_avanzado_2/83.png)

![imagen84](./images/servidor_web_avanzado_2/84.png)

![imagen85](./images/servidor_web_avanzado_2/85.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

Instalar CMS Drupal desde el navegador siguiendo los pasos y consultando documentación en Internet.

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

Configuración y creación del sitio Drupal: configurar idioma español; instalar módulo gtranslate y habilitar traducción a varios idiomas; instalar y configurar temas Marinelli, Zen y Fusion; crear dos o tres páginas de contenido, crear menú Primary Links y colocar como bloque. Otras opciones de configuración que desees.

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

---

## **Instalación Y Configuración De Aplicaciones Web Integradas.**

Eligimos una de las siguientes aplicaciones web integradas basadas en software libre y realiza, en grupos de hasta tres alumnos, su instalación y configuración en tu servidor web, siempre en modo remoto, desde el cliente W7 (excepto la creación del sitio web IIS –subdominio de miEmpresa-, carpeta física y configuración DNS y FTP necesarios).

* Blog: Wordpress

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

![imagen86](./images/servidor_web_avanzado_2/86.png)

---
