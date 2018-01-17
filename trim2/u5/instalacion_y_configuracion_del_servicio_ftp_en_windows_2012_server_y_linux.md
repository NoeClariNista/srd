___

# **Instalación Y Configuración Del Servicio FTP En Windows 2012 Server.**

---

Desinstalamos el Filezilla en Windows 2012 Server.

Instalamos el Servicio FTP en Windows 2012 Server, a través de Agregar roles y características (IIS).

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen001](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/001.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen002](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/002.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen003](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/003.png)

![imagen004](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/004.png)

![imagen005](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/005.png)

![imagen006](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/006.png)

![imagen007](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/007.png)

![imagen008](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/008.png)

Finalmente terminamos la instalación del Servicio FTP en Windows 2012 Server.

![imagen009](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/009.png)

Accedemos a la creación y configuración de Sitios FTP por medio de la Administración de IIS.

Debemos ir a Herramientas y luego a Administrador de Internet Information Services (IIS) para poder crear tres nuevos sitios FTP.

![imagen010](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/010.png)

![imagen011](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/011.png)

Creamos tres nuevos sitios FTP, en todos ellos debemos poder acceder a través de la IP del Servidor, 172.18.20.11.

![imagen012](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/012.png)

* Primer Sitio FTP.

  ![imagen013](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/013.png)

  El primero dominio estará asociado a la unidad C: completa.

  ![imagen014](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/014.png)

  Sin uso de SSL.

  ![imagen015](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/015.png)

  No se debe permitir accesos anónimos. Sólo el usuario Administrador podrá acceder al sitio. Modos de lectura y de escritura.

  ![imagen016](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/016.png)

  ![imagen017](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/017.png)

  * Examinamos todas las opciones de configuración de la página principal de tu Sitio FTP (IIS) y vemos lo siguiente.

    El Aislamiento de usuario FTP es para que un usuario no pueda acceder a carpetas anteriores del árbol.

    La autentificación FTP es para dar acceso anónimo o acceso básico.

    La compatibilidad con el firewall es para comprobar el firewall.

    La configuración SSL de FTP es para configurar los certificados SSL.

    El examen de directorios es para ver como es el estilo de la lista de directorios.

    El filtrado de solicitudes es para no permitir a ciertas máquinas.

    Los mensajes de FTP.

    El registro FTP es donde se guarda el registro de los errores y accesos de nuestro FTP.

    Las reglas de autorización son las distintas reglas de permisos a los usuarios.

    Las restricciones direcciones IP.

    Las sesiones actuales son las sesiones activas en este momento.

  * Tratamos de acceder al sitio FTP desde el propio Servidor a través de un navegador. Comprobamos accesos permitidos y denegados, por ejemplo, con otro usuario que no exista en nuestro Servidor y como ningún usuario con ninguna contraseña.

    ![imagen018](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/018.png)

    ![imagen019](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/019.png)

    ![imagen020](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/020.png)

    ![imagen021](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/021.png)

    ![imagen022](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/022.png)

    ![imagen023](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/023.png)

    ![imagen024](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/024.png)

  * Accedemos ahora desde un Cliente Windows de la misma forma. Realizamos las mismas comprobaciones que en el Servidor.

    ![imagen025](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/025.png)

    ![imagen026](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/026.png)

    ![imagen027](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/027.png)

    ![imagen028](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/028.png)

  * Instalamos el software WinSCP en el Cliente Windows.

    ![imagen029](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/029.png)

    ![imagen030](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/030.png)

    ![imagen031](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/031.png)

    ![imagen032](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/032.png)

    ![imagen033](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/033.png)

    ![imagen034](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/034.png)

    ![imagen035](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/035.png)

    ![imagen036](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/036.png)

    ![imagen037](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/037.png)

  * Configuramos la conexión al sitio FTP y tratamos de establecer conexión y realizamos comprobaciones.

    ![imagen038](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/038.png)

    ![imagen039](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/039.png)

* Segundo Sitio FTP.

  ![imagen040](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/040.png)

  El segundo dominio estará asociado al directorio wwwroot de Inetpub.

  ![imagen041](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/041.png)

  Habilitamos en este caso la posibilidad de conexiones SSL asociadas a uno de los certificados que poseemos en IIS.

  ![imagen042](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/042.png)

  No permitimos acceso anónimo y se permitirá el acceso a todos los usuarios de Active Directory en modo lectura y escritura.

  ![imagen043](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/043.png)

  ![imagen044](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/044.png)

  * Realizamos comprobaciones válidas e inválidas de conexión y operaciones, tanto desde el Servidor como desde el Cliente, por ejemplo, con el usuario Administrador, con otro usuario que no exista en nuestro Servidor y como ningún usuario con ninguna contraseña.

    ![imagen045](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/045.png)

    ![imagen046](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/046.png)

    ![imagen047](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/047.png)

    ![imagen048](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/048.png)

    ![imagen049](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/049.png)

    ![imagen050](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/050.png)

    ![imagen051](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/051.png)

    ![imagen052](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/052.png)

    ![imagen053](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/053.png)

    ![imagen054](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/054.png)

    ![imagen055](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/055.png)

  * Realizamos una configuración de conexión SSL desde WinSCP.

    ![imagen056](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/056.png)

    ![imagen057](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/057.png)

    ![imagen058](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/058.png)

* Tercer Sitio FTP.

  ![imagen059](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/059.png)

  El tercer dominio estará asociado a una carpeta cualquiera del Servidor que contenga información (archivos y carpetas), pero que no sea importante.

  ![imagen060](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/060.png)

  ![imagen061](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/061.png)

  Permitiremos acceso anónimo y sólo se podrá consultar y leer.

  ![imagen062](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/062.png)

  ![imagen063](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/063.png)

  * Comprobamos desde el Servidor y desde el Cliente.

    ![imagen064](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/064.png)

    ![imagen065](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/065.png)

    ![imagen066](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/066.png)

  * Realizamos una configuración de conexión SSL desde WinSCP.

    ![imagen067](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/067.png)

    ![imagen068](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/068.png)

    ![imagen069](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/069.png)

    ![imagen070](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/070.png)

Debemos crear un nuevo registro DNS que permita acceder a nuestro sitio FTP a través de la dirección ftp.pc20.edu.

![imagen071](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/071.png)

![imagen072](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/072.png)

![imagen073](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/073.png)

En un principio es posible que debas detener un sitio web para que pueda iniciarse otro. Tras comprobar el funcionamiento por separado de los sitios, hemos encontrado una solución para que nuestro Servidor ofrezca varios sitios FTP simultáneamente. Para poder realizar esta acción tenemos que darles a cada sitio FTP un puerto diferente.

* Segundo Sitio FTP.

  ![imagen074](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/074.png)

  ![imagen075](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/075.png)

  ![imagen076](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/076.png)

* Tercer Sitio FTP.

  ![imagen077](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/077.png)

  ![imagen078](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/078.png)

  ![imagen079](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/079.png)

Realizamos comprobaciones válidas de conexión tanto desde el Servidor como desde el Cliente.

* Desde el Servidor.

  ![imagen080](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/080.png)

  ![imagen081](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/081.png)

  ![imagen082](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/082.png)

  ![imagen083](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/083.png)

  ![imagen084](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/084.png)

  ![imagen085](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/085.png)

  ![imagen086](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/086.png)

  ![imagen087](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/087.png)

* Desde el Cliente.

  ![imagen088](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/088.png)

  ![imagen089](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/089.png)

  ![imagen090](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/090.png)

  ![imagen091](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/091.png)

  ![imagen092](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/092.png)

Realizamos una configuración de conexión SSL desde WinSCP de los tres sitios FTP.

![imagen093](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/093.png)

![imagen094](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/094.png)

![imagen095](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/095.png)

![imagen096](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/096.png)

![imagen097](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/097.png)

![imagen098](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/098.png)

![imagen099](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/099.png)

![imagen100](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/100.png)

![imagen101](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/101.png)

---

# **Instalación Y Configuración Del Servicio FTP En Linux.**

---

Instalamos el Servicio SSH en el Servidor Linux.

![imagen102](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/102.png)

Creamos dos usuarios en el sistema.

![imagen103](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/103.png)

Comprobamos, desde una máquina Cliente, acceso de los usuarios mediante ssh. Tratamos de ejecutar una aplicación gráfica del servidor de forma remota, desde el Cliente, mediante ssh, para ello instalamos el geany.

![imagen104](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/104.png)

![imagen105](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/105.png)

Accedemos, también desde el Cliente, mediante sftp al sistema de ficheros del Servidor y probar acceso, carga y descarga de archivos con ambos usuarios.

![imagen106](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/106.png)

Realizamos varias copias de archivos hacia / desde el servidor mediante scp, utilizando también los dos usuarios creados anteriormente.

![imagen107](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/107.png)

![imagen108](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/108.png)

![imagen109](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/109.png)

![imagen110](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/110.png)

![imagen111](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/111.png)

![imagen112](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/112.png)

Instalamos el paquete proftpd.

![imagen113](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/113.png)

![imagen114](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/114.png)

Tratamos de conectar al servicio ftp gestionado por proftpd tanto desde el Servidor como desde un Cliente. También probamos el acceso al ftp mediante los usuarios creados y realizando diferentes operaciones de listado, subida y descarga de archivos.

![imagen115](./images/instalacion_y_configuracion_del_servicio_ftp_en_windows_2012_server_y_linux/115.png)

---
