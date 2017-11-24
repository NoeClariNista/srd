___

# **Servidor Web Avanzado 2.**

## **Instalación De PHP, MySQL Y PHPMyAdmin.**

* Vamos a realizar las instalaciones y configuraciones necesarias para obtener un Servidor Web con soporte PHP y accesos a bases de datos relacionales, acceso FTP y gestor de bases de datos. Sobre este servidor, podremos realizar instalaciones de aplicaciones integradas (CMS, e-commerce, etc) desde el propio servidor o en modo remoto desde un cliente W7.

* Siguiendo los pasos detallados en las guías y tutoriales, instala soporte para PHP para tus sitios Web gestionados por IIS. Recomendado PHP 5.x VCx Non Thread-Safe (con IIS Fast CGI). PHP puede ser instalado de dos formas:

  * Utilizando   MSI   Installer   para   Windows:   Descargar   archivo   Installer   en
http://windows.php.net/download/ y       seguir       los       pasos       (ver
http://www.php.net/manual/es/install.windows.installer.msi.php). Configurar luego IIS para
que admita el fichero index.php por defecto en las carpetas y/o sitios que nos interese.

* Comprobar la instalación correcta de PHP colocando un fichero index.php en el sitio web destinado
a gestionar el CMS Drupal (www.miEmpresa.com ó miEmpresa\principal) con el siguiente código:
<?php phpinfo(); ?>

Siguiendo los pasos detallados en las guías y tutoriales, instala el servidor de bases de datos
relacionales MySQL para tus sitios Web gestionados por IIS. Descargar para ello el paquete
instalador de
http://dev.mysql.com/downloads/installer/
.
o
Descargar  e instalar
.NET Framework 4.0
.
o
Instalar MySQL y complementos necesarios.

Siguiendo los pasos detallados en las guías y tutoriales, instala PHPMyAdmin para tus sitios Web
gestionados   por   IIS.   Para   esto   debes   crear   un   nuevo   sitio   web   asociado   a
phpmyadmin.miEmpresa.com,   recordando   crear   la   correspondiente   carpeta   (donde
descomprimirás los ficheros de phpMyAdmin) y actualizar DNS.

---

Práctica de Windows 2012 Server -
 SRD
– 2º ASIR
Instalación y Configuración de un Servidor Web Avanzado
Internet Information Server
– Instalación de Servidor FTP y CMS Drupal
•
Siguiendo los pasos detallados en las guías y tutoriales proporcionados:
o
Instalar Servidor FTP FileZilla en Windows 2012 Server.
o
Crear un usuario denominado ftpuser en el Servidor FTP y asociarle a este usuario permisos
de Control Total sobre la carpeta en la que se va a instalar el CMS de miEmpresa.
o
Crear un nuevo registro DNS
 que permita acceder a nuestro sitio FTP a través de la dirección
ftp.miEmpresa.com.
•
A partir de este punto, salvo problemas de difícil solución, todo el trabajo deberá realizarse en
modo remoto, desde el cliente Windows 7:
o
Comprobar acceso a phpMyAdmin de
sde un navegador (phpmyadmin.miEmpresa.com).
o
Descargar  CMS Drupal de
drupal.org
.
o
Comprobar el acceso al sitio FTP creado a través de un navegador y con el usuario ftpuser.
o
Instalar un cliente ftp (p.e.: FileZilla) e
n Windows 7 para poder realizar todas las operaciones
sobre los ficheros y carpetas del servidor web.
o
Descomprimir  y subir archivos Drupal a carpeta principal (www.miEmpresa.com).
o
Crear una nueva base de datos, denominada cms, a través de phpMyAdmin.
o
Crea
r usuario cms y asignar todos los privilegios para la base de datos anterior.
o
Instalar  CMS  Drupal  desde  el  navegador  siguiendo  los  pasos  y  consultando  documentación  
en Internet.
o
Configuración   y   creación   del   sitio   Drupal:   configurar   idioma   español;   instalar
módulo
gtranslate y habilitar traducción a varios idiomas; instalar y configurar temas Marinelli, Zen y
Fusion;  crear  dos  o  tres  páginas  de  contenido,  crear  menú  Primary  Links  y  colocar  como  
bloque. Otras opciones de configuración que desees.

---

Práctica de Windows 2012 Server -
 SRD
– 2º ASIR
Instalación y Configuración de un Servidor Web Avanzado
Instalación y Configuración de Aplicaciones Web Integradas
•
Elige  una  de  las  siguientes  aplicaciones  web  integradas  basadas  en  software  libre  y  
realiza,  en  grupos  de  hasta  tres  alumnos,  su  instalación  y  configuración  en  tu  servidor  
web, siempre en modo remoto, desde el cliente W7 (excepto la creación del sitio web IIS
–subdominio  de  miEmpresa
-,  carpeta  física  y  configuración  DNS  y  FTP  necesarios).
Consulta la amplia documentación disponible en Internet.:
o
Galería fotográfica: Gallery o Coppermine.
o
Tienda Virtual: osCommerce
o
Formación online: Moodle
o
Blog: Wordpress
o
Foros: SMF

---
