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

Lo primero que tenemos que hacer es ir a panel de Administración de Servidor, vamos a agregar roles/características y agregamos el rol de CGI, con esto nos descargaremos IIS Fast CGI.

![imagen001](./images/servidor_web_avanzado_2/001.png)

![imagen002](./images/servidor_web_avanzado_2/002.png)

Instalamos el soporte para PHP para tus sitios Web gestionados por IIS. Nos descargarmos la versión de PHP 5.3.9-nts-Win32-VC9-x86.msi, para ello vamos a la página de [PHP](windows.php.net/downloads/releases/archives).

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen003](./images/servidor_web_avanzado_2/003.png)

![imagen004](./images/servidor_web_avanzado_2/004.png)

![imagen005](./images/servidor_web_avanzado_2/005.png)

![imagen006](./images/servidor_web_avanzado_2/006.png)

![imagen007](./images/servidor_web_avanzado_2/007.png)

![imagen008](./images/servidor_web_avanzado_2/008.png)

Comprobamos la instalación correcta de PHP colocando un fichero index.php en el sitio web destinado a gestionar el CMS Drupal, www.miEmpresa.com, con el siguiente código: `<?php phpinfo(); ?>`.

![imagen009](./images/servidor_web_avanzado_2/009.png)

![imagen010](./images/servidor_web_avanzado_2/010.png)

Vamos a un navegador, ponemos www.miempresa.com y tenemos que ver que funciona.

![imagen011](./images/servidor_web_avanzado_2/011.png)

Instalamos el Servidor de bases de datos relacionales MySQL para tus sitios Web gestionados por IIS. Descargamos para ello el paquete instalador de [MySQL](http://dev.mysql.com/downloads/installer/). Instalamos MySQL y los complementos que creemos necesarios.

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen012](./images/servidor_web_avanzado_2/012.png)

![imagen013](./images/servidor_web_avanzado_2/013.png)

![imagen014](./images/servidor_web_avanzado_2/014.png)

Descargamos e instalamos .NET Framework 4.0.

![imagen015](./images/servidor_web_avanzado_2/015.png)

![imagen016](./images/servidor_web_avanzado_2/016.png)

Seguimos los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen017](./images/servidor_web_avanzado_2/017.png)

![imagen018](./images/servidor_web_avanzado_2/018.png)

![imagen019](./images/servidor_web_avanzado_2/019.png)

![imagen020](./images/servidor_web_avanzado_2/020.png)

![imagen021](./images/servidor_web_avanzado_2/021.png)

![imagen022](./images/servidor_web_avanzado_2/022.png)

![imagen023](./images/servidor_web_avanzado_2/023.png)

Creamos un nuevo usuario dentro del Servidor de bases de datos relacionales MySQL.

![imagen024](./images/servidor_web_avanzado_2/024.png)

Seguimos los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen025](./images/servidor_web_avanzado_2/025.png)

![imagen026](./images/servidor_web_avanzado_2/026.png)

![imagen027](./images/servidor_web_avanzado_2/027.png)

![imagen028](./images/servidor_web_avanzado_2/028.png)

![imagen029](./images/servidor_web_avanzado_2/029.png)

Finalmente ya tenemos instalado el Servidor de bases de datos relacionales MySQL.

![imagen030](./images/servidor_web_avanzado_2/030.png)

Abrimos una consola de MySQL y nos conectamos con el usuario que creamos anteriormente.

![imagen031](./images/servidor_web_avanzado_2/031.png)

Instalamos PHPMyAdmin para tus sitios Web gestionados por IIS. Para esto debemos crear un nuevo sitio web asociado a phpmyadmin.miEmpresa.com, recordando crear la correspondiente carpeta, donde descomprimiremos los ficheros de phpMyAdmin, y actualizamos los DNS. Descargamos para ello el paquete instalador de [phpMyAdmin](http://www.phpmyadmin.net/home_page/downloads.php)

![imagen032](./images/servidor_web_avanzado_2/032.png)

![imagen033](./images/servidor_web_avanzado_2/033.png)

![imagen034](./images/servidor_web_avanzado_2/034.png)

![imagen035](./images/servidor_web_avanzado_2/035.png)

![imagen036](./images/servidor_web_avanzado_2/036.png)

Ponemos en un navegador phpmyadmin.miempresa.com y nos tiene que salir la página de phpMyAdmin.

![imagen037](./images/servidor_web_avanzado_2/037.png)

Ponemos el usuario que ya hemos creado.

![imagen038](./images/servidor_web_avanzado_2/038.png)

Finalmente entramos en phpMyAdmin.

![imagen039](./images/servidor_web_avanzado_2/039.png)

---

## **Instalación De Servidor FTP Y CMS Drupal.**

Instalamos Servidor FTP FileZilla en Windows 2012 Server. Nos descargamos Filezilla en desde la página de [Filezilla](http://filezilla-project.org/download.php?type=server).

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen040](./images/servidor_web_avanzado_2/040.png)

![imagen041](./images/servidor_web_avanzado_2/041.png)

![imagen042](./images/servidor_web_avanzado_2/042.png)

![imagen043](./images/servidor_web_avanzado_2/043.png)

![imagen044](./images/servidor_web_avanzado_2/044.png)

![imagen045](./images/servidor_web_avanzado_2/045.png)

![imagen046](./images/servidor_web_avanzado_2/046.png)

Creamos un usuario denominado `ftpuser` en el Servidor FTP y le asociamos a este usuario permisos de Control Total sobre la carpeta en la que se va a instalar el CMS de miEmpresa.

![imagen047](./images/servidor_web_avanzado_2/047.png)

![imagen048](./images/servidor_web_avanzado_2/048.png)

![imagen049](./images/servidor_web_avanzado_2/049.png)

Creamos un nuevo registro DNS que nos permita acceder a nuestro sitio FTP a través de la dirección `ftp.miEmpresa.com`.

![imagen050](./images/servidor_web_avanzado_2/050.png)

![imagen051](./images/servidor_web_avanzado_2/051.png)

Comprobamos el acceso al sitio FTP a través de un navegador desde localhost y a tráves de la dirección `ftp.miEmpresa.com`, todo esto conectandonos con el usuario que hemos creado anteriormente.

![imagen052](./images/servidor_web_avanzado_2/052.png)

![imagen053](./images/servidor_web_avanzado_2/053.png)

![imagen054](./images/servidor_web_avanzado_2/054.png)

![imagen055](./images/servidor_web_avanzado_2/055.png)

A partir de ahora realizaremos todo desde el cliente Windows 10.

Comprobamos el acceso a phpMyAdmin desde un navegador, phpmyadmin.miEmpresa.com.

![imagen056](./images/servidor_web_avanzado_2/056.png)

![imagen057](./images/servidor_web_avanzado_2/057.png)

![imagen058](./images/servidor_web_avanzado_2/058.png)

Descargamos CMS Drupal de drupal.org. Nos descargamos Drupal desde la página de [Drupal](http://drupal.org/project/drupal)

Comprobamos el acceso al sitio FTP creado a través de un navegador y con el usuario ftpuser. Antes de comprobarlo tenemos que añadir unas reglas de entrada y de salida al Firewall para que nos permita conectar el Cliente con el Servidor.

* Regla de entrada.

![imagen059](./images/servidor_web_avanzado_2/059.png)

![imagen060](./images/servidor_web_avanzado_2/060.png)

![imagen061](./images/servidor_web_avanzado_2/061.png)

![imagen062](./images/servidor_web_avanzado_2/062.png)

* Regla de salida.

![imagen063](./images/servidor_web_avanzado_2/063.png)

![imagen064](./images/servidor_web_avanzado_2/064.png)

![imagen065](./images/servidor_web_avanzado_2/065.png)

![imagen066](./images/servidor_web_avanzado_2/066.png)

Intentamos acceder a tráves de un navegador y con el usuario ftpuser.

![imagen067](./images/servidor_web_avanzado_2/067.png)

![imagen068](./images/servidor_web_avanzado_2/068.png)

Instalamos un Cliente FTP, FileZilla, en Windows 10 para poder realizar todas las operaciones sobre los ficheros y carpetas del servidor web. Nos descargamos Filezilla en la página de [Filezilla](http://filezilla-project.org/download.php?type=client).

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen069](./images/servidor_web_avanzado_2/069.png)

![imagen070](./images/servidor_web_avanzado_2/070.png)

![imagen071](./images/servidor_web_avanzado_2/071.png)

![imagen072](./images/servidor_web_avanzado_2/072.png)

![imagen073](./images/servidor_web_avanzado_2/073.png)

Descomprimimos y subimos archivos Drupal a carpeta principal, www.miEmpresa.com.

![imagen074](./images/servidor_web_avanzado_2/074.png)

![imagen075](./images/servidor_web_avanzado_2/075.png)

![imagen076](./images/servidor_web_avanzado_2/076.png)

![imagen077](./images/servidor_web_avanzado_2/077.png)

Creamos una nueva base de datos, denominada cms, a través de phpMyAdmin.

![imagen078](./images/servidor_web_avanzado_2/078.png)

![imagen079](./images/servidor_web_avanzado_2/079.png)

Creamos usuario cms y asignamos todos los privilegios para la base de datos anterior.

![imagen080](./images/servidor_web_avanzado_2/080.png)

![imagen081](./images/servidor_web_avanzado_2/081.png)

![imagen082](./images/servidor_web_avanzado_2/082.png)

![imagen083](./images/servidor_web_avanzado_2/083.png)

![imagen084](./images/servidor_web_avanzado_2/084.png)

![imagen085](./images/servidor_web_avanzado_2/085.png)

Instalamos CMS Drupal desde el navegador siguiendo los pasos.

![imagen086](./images/servidor_web_avanzado_2/086.png)

![imagen087](./images/servidor_web_avanzado_2/087.png)

Vamos al Servidor a mi empresa y cambiamos la extensión del siguiente archivo porque nos da problemas en la instalación.

![imagen088](./images/servidor_web_avanzado_2/088.png)

![imagen089](./images/servidor_web_avanzado_2/089.png)

Nos descargamos el idioma Spanish.

![imagen090](./images/servidor_web_avanzado_2/090.png)

![imagen091](./images/servidor_web_avanzado_2/091.png)

Guardamos el archivo en el Servidor, en concreto, en translations.

![imagen092](./images/servidor_web_avanzado_2/092.png)

![imagen093](./images/servidor_web_avanzado_2/093.png)

Nos da un error, lo que tenemos que hacer es copiar el archivo que nos dice.

![imagen094](./images/servidor_web_avanzado_2/094.png)

Le accionamos Permisos de modificar, lectura, escritura y ejecución a Todos.

![imagen095](./images/servidor_web_avanzado_2/095.png)

![imagen096](./images/servidor_web_avanzado_2/096.png)

![imagen097](./images/servidor_web_avanzado_2/097.png)

![imagen098](./images/servidor_web_avanzado_2/098.png)

![imagen099](./images/servidor_web_avanzado_2/099.png)

![imagen100](./images/servidor_web_avanzado_2/100.png)

![imagen101](./images/servidor_web_avanzado_2/101.png)

![imagen102](./images/servidor_web_avanzado_2/102.png)

Configuramos el sitio Drupal.

Nos da un error en la una carpeta porque no se puede crear un archivo vamos a esa carpeta.

![imagen103](./images/servidor_web_avanzado_2/103.png)

![imagen104](./images/servidor_web_avanzado_2/104.png)

Cambiamos los permisos de los usuarios y añadimos modificar.

![imagen105](./images/servidor_web_avanzado_2/105.png)

![imagen106](./images/servidor_web_avanzado_2/106.png)

Creamos dos o tres páginas de contenido, creamos menú Primary Links y lo colocamos como bloque.

![imagen107](./images/servidor_web_avanzado_2/107.png)

![imagen108](./images/servidor_web_avanzado_2/108.png)

![imagen109](./images/servidor_web_avanzado_2/109.png)

![imagen110](./images/servidor_web_avanzado_2/110.png)

![imagen111](./images/servidor_web_avanzado_2/111.png)

![imagen112](./images/servidor_web_avanzado_2/112.png)

![imagen113](./images/servidor_web_avanzado_2/113.png)

![imagen114](./images/servidor_web_avanzado_2/114.png)

![imagen115](./images/servidor_web_avanzado_2/115.png)

Instalamos módulo gtranslate y habilitamos traducción a varios idiomas.

![imagen116](./images/servidor_web_avanzado_2/116.png)

Instalamos y configuramos el tema Marinelli.

![imagen117](./images/servidor_web_avanzado_2/117.png)

![imagen118](./images/servidor_web_avanzado_2/118.png)

![imagen119](./images/servidor_web_avanzado_2/119.png)

![imagen120](./images/servidor_web_avanzado_2/120.png)

![imagen121](./images/servidor_web_avanzado_2/121.png)

---

## **Instalación Y Configuración De Aplicaciones Web Integradas.**

Eligimos una de las aplicaciones web integradas basadas en software libre y realizamos su instalación y configuración en el Servidor web, siempre en modo remoto, desde el cliente W10, excepto la creación del sitio web IIS, carpeta física y configuración DNS y FTP necesarios. [Wordpress](http://wordpress.org/download/).

![imagen122](./images/servidor_web_avanzado_2/122.png)

![imagen123](./images/servidor_web_avanzado_2/123.png)

![imagen124](./images/servidor_web_avanzado_2/124.png)

![imagen125](./images/servidor_web_avanzado_2/125.png)

![imagen126](./images/servidor_web_avanzado_2/126.png)

![imagen127](./images/servidor_web_avanzado_2/127.png)

![imagen128](./images/servidor_web_avanzado_2/128.png)

![imagen129](./images/servidor_web_avanzado_2/129.png)

![imagen130](./images/servidor_web_avanzado_2/130.png)

![imagen131](./images/servidor_web_avanzado_2/131.png)

![imagen132](./images/servidor_web_avanzado_2/132.png)

![imagen133](./images/servidor_web_avanzado_2/133.png)

![imagen134](./images/servidor_web_avanzado_2/134.png)

---
