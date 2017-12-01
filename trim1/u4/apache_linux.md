Práctica Servidor Web Apache - Linux


Indicaciones para realizar las prácticas de instalación y configuración de un servidor web Apache en Linux. Las prácticas deben realizarse individualmente y debe elaborarse un informe que se entregará al finalizar las mismas. Este informe debe incluir los pasos realizados, capturas de pantalla y debe hacer especial hincapié en los problemas encontrados y las soluciones aportadas. A continuación se detallan las tareas a realizar así como algunos datos y enlaces de interés, a partir de los cuales se debe investigar y descubrir, con los medios a tu alcance, todo lo necesario para obtener los resultados deseados.

    A través de varias prácticas se pretende obtener un conjunto de sitios web similares a los realizados en IIS, es decir, algo semejante a lo siguiente:
        Dominio principal: miempresa.com (o similar)
        Alias página principal: www.miempresa.com
        Sitio seguro (https): pagos.miempresa.com (o miempresa.com/pagos)
        Carpetas privadas protegidas: empleados.miempresa.com (o miempresa.com/empleados)
        Instalación PHP, MySQL, phpMyAdmin
        Gestión bases de datos: phpmyadmin.miempresa.com (o miempresa.com/phpmyadmin)
        Instalación FTP o SSH (opcional)
        Instalación y configuración plataforma Drupal, Joomla, Moodle, Gallery, osCommerce, etc. en página principal

Para ello tienes que seguir los siguientes pasos. Es indistinto el orden en que realices las prácticas, teniendo en cuenta que hay pasos que si que hay que realizar antes o después que otros:

    Configurar MV Ubuntu o similar en adaptador Puente (acceso a Internet)


    Apache:
        Instalar Apache: sudo apt-get install apache2
        Comprobar carpeta raíz sitio web: /var/www
        Comprobar acceso a localhost //It works!
        Añadir línea www.miempresa.com asociada a IP servidor en /etc/hosts o servidor DNS. Comprobar acceso
        Reiniciar apache: sudo /etc/init.d/apache2 restart ó reload
        Error + Access logs: /var/log/apache2


    PHP
        Instalar php: sudo apt-get install php5
        Comprobar acceso a index.php -<?php phpinfo(); ?>-
        sudo apt-get install libapache2-mod-php5 //No debe ser necesario


    Crear Hosts Virtuales en Apache, es decir, asociar carpetas con sitios web (ej: empleados.miempresa.com --> /var/www/empleados) y establecer configuración (/etc/apache2/sites-available/000-default.conf)
        Configuración Hosts Virtuales (sitios web independientes) en este enlace:
        Ejemplo:

<VirtualHost *:80>

ServerAdmin webmaster@miempresa.com

ServerName empleados.miempresa.com //Añadir también a hosts o serviodor DNS

DocumentRoot /var/www/empleados

<Directory /var/www/empleados> // No es necesario para VirtualHost sencillos

Opciones típicas...

</Directory>

</VirtualHost>


    Configurar sitio web seguro pagos:
        Al instalar Apache, se instala también SSL
        Generar certificado autofirmado:
            § openssl genrsa -des3 -out server.key 1024
            § openssl rsa -in server.key -out server.pem
            § openssl req -new -key server.key -out server.csr
            § openssl x509 -req -days 360 -in server.csr -signkey server.key -out server.crt
        Modificar /etc/apache2/sites-available/000-default.conf según indicaciones PDF para crear host virtual seguro
        Consultar alternativas al PDF (Host Virtual) en este enlace
        Habilitar módulo SSL apache: sudo a2enmod ssl


    Acceso a carpetas privadas

        Autenticación mediante .htaccess: Ver enlace
        Estructura: empleados.miemepresa.com (acceso a todos los empleados pero no anónimos) y subcarpetas personales de empleados (dos o tres, con acceso limitado al usuario)



    MySQL
        Instalar MySQL: sudo apt-get install mysql-server
        Instalar soporte php para MySQL: sudo apt-get install php5-mysql //Puede no ser necesario


    phpMyAdmin
        Descargar última versión (tar.gz) desde phpmyadmin.net, descomprimir en subcarpeta de /var/www (u otra asociada por host virtual) y comprobar acceso


    Plataforma Drupal / Joomla / Moodle / etc
        Creación bases de datos y usuarios necesarios
        Instalación /configuración FTP y/o SSH para acceso remoto desde cliente (opcional)
        Descarga, instalación y configuración plataforma Drupal, Joomla, Moodle, Gallery, osCommerce, etc. en página principal.
