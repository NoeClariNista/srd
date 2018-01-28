___

# **Práctica Servicio SMTP Windows 2012 Server.**

---

## **Instalación Y Configuración De Un Servidor De Correo SMTP.**

---

Instalamos el Servicio SMTP en Windows 2012 Server utilizando el Asistente.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen001](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/001.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen002](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/002.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen003](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/003.png)

![imagen004](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/004.png)

![imagen005](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/005.png)

![imagen006](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/006.png)

![imagen007](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/007.png)

![imagen008](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/008.png)

![imagen009](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/009.png)

Finalmente terminamos la instalación del Servicio SMTP en Windows 2012 Server.

![imagen010](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/010.png)

La configuración del Servicio SMTP la haremos a través del Administrador de aplicaciones (IIS) 6.0.

Lo que tenemos que hacer es ir a Administrador del Servidor.

![imagen011](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/011.png)

Luego tenemos que ir a Herramientas y vamos a Administrador de Internet Information Services (IIS) 6.0.

![imagen012](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/012.png)

![imagen013](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/013.png)

Realizamos la configuración en las propiedades de SMTP.

![imagen014](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/014.png)

* Establecemos como IP todas las asignadas, en mi caso, 172.18.20.11. Limitamos el número de conexiones a 50. Habilitamos el registro en formato W3C, diario y en una carpeta determinada.

  ![imagen015](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/015.png)

  ![imagen016](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/016.png)

* Configuramos el envío de mensajes dentro de nuestra red local. Aceptamos la conexión al Servidor y la retransmisión de mensajes a todos los equipos menos los que aparecen en la lista, incluimos una IP cualquiera en la lista para impedir su acceso y retransmisión, en concreto la 172.18.20.20.

  ![imagen017](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/017.png)

  ![imagen018](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/018.png)

  ![imagen019](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/019.png)

  ![imagen020](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/020.png)

  ![imagen021](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/021.png)

  ![imagen022](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/022.png)

* Establecemos la autenticación anónima.

  ![imagen023](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/023.png)

  ![imagen024](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/024.png)

* Echamos un vistazo al resto de opciones de configuración del Servidor.

  ![imagen025](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/025.png)

  ![imagen026](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/026.png)

  ![imagen027](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/027.png)

  ![imagen028](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/028.png)

* Aplicamos cambios y reiniciamos el Servicio.

  ![imagen029](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/029.png)

  ![imagen030](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/030.png)

  ![imagen031](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/031.png)

  ![imagen032](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/032.png)

* Comprobamos la existencia del dominio AD predeterminado. Creamos un dominio de tipo alias para disponer de cuentas en otro dominio.

  ![imagen033](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/033.png)

  ![imagen034](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/034.png)

  ![imagen035](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/035.png)

  ![imagen036](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/036.png)

  ![imagen037](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/037.png)

* Creamos un nuevo DNS.

  Lo primero que tenemos que hacer es ir a Administrador del Servidor.

  ![imagen038](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/038.png)

  Luego a DNS para poder crear una nueva zona de búsqueda directa en el Servidor.

  ![imagen039](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/039.png)

  ![imagen040](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/040.png)

  Creamos una zona de búsqueda directa.

  ![imagen041](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/041.png)

  Nos sale el asistente para la nueva zona.

  ![imagen042](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/042.png)

  Elegimos el tipo de zona que queremos.

  ![imagen043](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/043.png)

  Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

  ![imagen044](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/044.png)

  Le ponemos un nombre a nuestra zona.

  ![imagen045](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/045.png)

  Permitimos actualizaciones dinámicas seguras.

  ![imagen046](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/046.png)

  Se ha creado la nueva zona.

  ![imagen047](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/047.png)

  Ya contamos con otra zona de búsqueda directa.

  ![imagen048](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/048.png)

  En la zona de búsqueda directa añadimos un host nuevo (A).

  ![imagen049](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/049.png)

  Un host para el Servidor denominado mail.

  ![imagen050](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/050.png)

  Ya tenemos este registro creado.

  ![imagen051](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/051.png)

* Comprobamos la carpetas de correo creados en `C:\Inetpub\mailroot`.

  ![imagen052](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/052.png)

  * En el Cliente Windows.

    Comprobamos el acceso al nuevo nombre DNS creado en el Servidor.

    ![imagen053](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/053.png)

    Configuramos el Cliente de correo Live mail agregando dos cuentas de correo cualesquiera. Deberemos especificar el usuario/buzón, la contraseña y el Servidor SMTP.

    ![imagen054](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/054.png)

    ![imagen055](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/055.png)

    ![imagen056](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/056.png)

    ![imagen057](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/057.png)

    ![imagen058](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/058.png)

    ![imagen059](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/059.png)

    ![imagen060](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/060.png)

    ![imagen061](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/061.png)

    ![imagen062](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/062.png)

    ![imagen063](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/063.png)

    ![imagen064](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/064.png)

    ![imagen065](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/065.png)

    Enviamos varios correos desde / hacia las diferentes cuentas y comprobar envío (real o ficticio) y carpetas mailroot. Las carpetas existentes en mailroot alojan mensajes en cola (Queue) y mensajes entregados (Drop).

    ![imagen066](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/066.png)

    ![imagen067](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/067.png)

    ![imagen068](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/068.png)

    ![imagen069](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/069.png)

    ![imagen070](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/070.png)

    ![imagen071](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/071.png)

    ![imagen072](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/072.png)

    ![imagen073](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/073.png)

    ![imagen074](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/074.png)

    ![imagen075](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/075.png)

    ![imagen076](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/076.png)

  * En el Servidor.

    Tenemos que añadir una nueva configuración de Servicio SMTP a través del administrador de aplicaciones (IIS) 6.0.

    Lo que tenemos que hacer es ir a Administrador del Servidor.

    ![imagen077](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/077.png)

    Luego tenemos que ir a Herramientas y vamos a Administrador de Internet Information Services (IIS) 6.0.

    ![imagen078](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/078.png)

    ![imagen079](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/079.png)

    Realizamos la configuración en las propiedades de SMTP.

    ![imagen080](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/080.png)

    ![imagen081](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/081.png)

    Establecemos la autenticación básica de Windows.

    ![imagen082](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/082.png)

    ![imagen083](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/083.png)

    Probamos diferentes configuraciones de dominio predeterminado, por ejemplo, cifrado TLS.

    ![imagen084](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/084.png)

    ![imagen085](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/085.png)

  * En el Cliente Windows.

    Configuramos las cuentas según los parámetros especificados en el Servidor.

    ![imagen086](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/086.png)

    ![imagen087](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/087.png)

    ![imagen088](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/088.png)

    ![imagen089](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/089.png)

    ![imagen090](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/090.png)

    ![imagen091](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/091.png)

    ![imagen092](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/092.png)

    ![imagen093](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/093.png)

    ![imagen094](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/094.png)

    ![imagen095](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/095.png)

    ![imagen096](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/096.png)

    ![imagen097](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/097.png)

    ![imagen098](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/098.png)

    ![imagen099](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/099.png)

    ![imagen100](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/100.png)

    ![imagen101](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/101.png)

    Enviamos varios correos desde / hacia las diferentes cuentas y comprobamos el envío y las carpetas mailroot. En este caso sólo tendrán acceso al servidor SMTP cuentas del dominio y correspondientes a usuarios de AD.

    ![imagen102](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/102.png)

    ![imagen103](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/103.png)

    ![imagen104](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/104.png)

    ![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

    ![imagen106](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/106.png)

    ![imagen107](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/107.png)

    ![imagen108](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/108.png)

    ![imagen109](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/109.png)

---

# **Práctica hMailServer Windows 2012 Server.**

---

## **Configuración De hMailServer En Windows Server 2012.**

---

Queremos configurar un Servidor de Correo para nuestra red local, para que los usuarios de nuestra red puedan comunicarse por correo electrónico.

En primer lugar, hay que desinstalar el Servicio SMTP de Windows 2012 Server.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen110](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/110.png)

Luego tenemos que ir a Administrar y vamos a Quitar roles y funciones.

![imagen111](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/111.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen112](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/112.png)

![imagen113](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/113.png)

![imagen114](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/114.png)

![imagen115](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/115.png)

![imagen116](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/116.png)

![imagen117](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/117.png)

Finalmente terminamos la desinstalación del Servicio SMTP en Windows 2012 Server.

![imagen118](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/118.png)

Ahora tenemos que instalar las Características de .NET Framework 3.5.

Lo que tenemos que hacer es ir a Administrador del Servidor.

![imagen119](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/119.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen120](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/120.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen121](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/121.png)

![imagen122](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/122.png)

![imagen123](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/123.png)

![imagen124](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/124.png)

![imagen125](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/125.png)

![imagen126](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/126.png)

![imagen127](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/127.png)

Finalmente terminamos la instalación de las Características de .Net Framework 3.5.

![imagen128](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/128.png)

Debemos descargar e instalar en el Servidor Windows 2012 Server el Servidor de Correo hMailServer.

Vamos a la página oficial de [hMailServer](https://www.hmailserver.com/).

![imagen129](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/129.png)

Vamos a la pestaña Download y nos descargamos hMailServer.

![imagen130](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/130.png)

El resto de pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen131](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/131.png)

![imagen132](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/132.png)

![imagen133](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/133.png)

![imagen134](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/134.png)

![imagen135](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/135.png)

![imagen136](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/136.png)

![imagen137](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/137.png)

![imagen138](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/138.png)

![imagen139](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/139.png)

Finalmente terminamos la instalación de hMailServer.

![imagen140](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/140.png)

Entramos en hMailServer.

![imagen141](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/141.png)

Ponemos la contraseña que pusimos durante la instalación de hMailServer.

![imagen142](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/142.png)

Creamos dos dominios denominados `srd.edu` y `asir.edu`.

Para añadir los dos nuevos dominios solo tenemos que pinchar en Añadir dominio.

![imagen143](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/143.png)

![imagen144](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/144.png)

![imagen145](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/145.png)

![imagen146](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/146.png)

![imagen147](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/147.png)

![imagen148](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/148.png)

Ejecutamos los diagnósticos para ambos dominios.

![imagen149](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/149.png)

* `asir.edu`.

![imagen150](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/150.png)

* `srd.edu`.

![imagen151](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/151.png)

Solucionamos el error de backup asignando una carpeta para tal fin. Para ello creamos la carpeta `C:\backup`. También establecemos una copia de seguridad de los mensajes.

![imagen152](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/152.png)

![imagen153](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/153.png)

![imagen154](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/154.png)

Ejecutamos los diagnósticos para ambos dominios denuevo.

* `asir.edu`.

![imagen155](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/155.png)

* `srd.edu`.

![imagen156](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/156.png)

Creamos dos cuentas para dos usuarios ficticios en cada uno de los dos dominios. Configuramos las cuentas con diferentes opciones, como por ejemplo, auto-reply y forwarding.

* `asir.edu`.

![imagen157](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/157.png)

![imagen158](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/158.png)

![imagen159](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/159.png)

![imagen160](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/160.png)

![imagen161](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/161.png)

![imagen162](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/162.png)

* `srd.edu`.

![imagen163](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/163.png)

![imagen164](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/164.png)

![imagen165](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/165.png)

![imagen166](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/166.png)

![imagen167](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/167.png)

![imagen168](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/168.png)

![imagen169](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/169.png)

![imagen170](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/170.png)

Configuramos el Servicio DNS para crear las entradas `mail.srd.edu` y `mail.asir.edu` que apunten a la dirección IP del Servidor Windows 2012, es decir, 172.18.20.11.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen171](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/171.png)

Luego a DNS para poder crear dos nuevas zonas de búsqueda directa en el Servidor.

![imagen172](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/172.png)

![imagen173](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/173.png)

Creamos una zona de búsqueda directa.

![imagen174](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/174.png)

Nos sale el asistente para la nueva zona.

![imagen175](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/175.png)

Elegimos el tipo de zona que queremos.

![imagen176](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/176.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen177](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/177.png)

Le ponemos un nombre a nuestra zona.

![imagen178](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/178.png)

Permitimos actualizaciones dinámicas seguras.

![imagen179](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/179.png)

Se ha creado la nueva zona.

![imagen180](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/180.png)

Ya contamos con otra zona de búsqueda directa.

![imagen181](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/181.png)

En la zona de búsqueda directa añadimos un host nuevo (A).

![imagen182](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/182.png)

Un host para el Servidor denominado mail.

![imagen183](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/183.png)

Ya tenemos este registro creado.

![imagen184](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/184.png)

En la zona de búsqueda directa añadimos un nuevo intercambio de correo (MX).

![imagen185](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/185.png)

Este nuevo registro estará apuntado al registro creado anteriormente.

![imagen186](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/186.png)

Ya tenemos este registro creado.

![imagen187](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/187.png)

Creamos una zona de búsqueda directa.

![imagen188](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/188.png)

Nos sale el asistente para la nueva zona.

![imagen189](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/189.png)

Elegimos el tipo de zona que queremos.

![imagen190](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/190.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen191](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/191.png)

Le ponemos un nombre a nuestra zona.

![imagen192](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/192.png)

Permitimos actualizaciones dinámicas seguras.

![imagen193](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/193.png)

Se ha creado la nueva zona.

![imagen194](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/194.png)

Ya contamos con otra zona de búsqueda directa.

![imagen195](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/195.png)

En la zona de búsqueda directa añadimos un host nuevo (A).

![imagen196](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/196.png)

Un host para el Servidor denominado mail.

![imagen197](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/197.png)

Ya tenemos este registro creado.

![imagen198](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/198.png)

En la zona de búsqueda directa añadimos un nuevo intercambio de correo (MX).

![imagen199](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/199.png)

Este nuevo registro estará apuntado al registro creado anteriormente.

![imagen200](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/200.png)

Ya tenemos este registro creado.

![imagen201](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/201.png)

Ejecutamos los diagnósticos para ambos dominios.

* `asir.edu`.

![imagen202](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/202.png)

* `srd.edu`.

![imagen203](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/203.png)

Realizamos todas las opciones de configuración que consideremos necesarias y convenientes, como por ejemplo, opciones de protocolos SMTP, bloqueo de correo entrante y logging.

![imagen204](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/204.png)

![imagen205](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/205.png)

![imagen206](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/206.png)

Configuramos en el Cliente W10 dos Clientes de correo como Live Mail para acceder al Servidor de correo instalado en Windows 2012.

![imagen207](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/207.png)

![imagen208](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/208.png)

![imagen209](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/209.png)

![imagen210](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/210.png)

![imagen211](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/211.png)

![imagen212](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/212.png)

![imagen213](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/213.png)

![imagen214](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/214.png)

![imagen215](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/215.png)

![imagen216](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/216.png)

![imagen217](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/217.png)

![imagen218](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/218.png)

![imagen219](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/219.png)

Realizamos pruebas de envío y recepción de correos entre los diferentes usuarios, comprobando, además de envío y recepción correctas, el efecto de las opciones configuradas en las cuentas.

![imagen220](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/220.png)

![imagen221](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/221.png)

![imagen222](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/222.png)

![imagen223](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/223.png)

![imagen224](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/224.png)

Creamos una lista de distribución asociada al dominio y añadimos a los dos usuarios de `asir.edu` a ella.

![imagen225](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/225.png)

![imagen226](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/226.png)

![imagen227](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/227.png)

![imagen228](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/228.png)

![imagen229](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/229.png)

![imagen230](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/230.png)

![imagen231](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/231.png)

Realizamos pruebas de envío y recepción de correos por medio de la lista de distribución.

![imagen232](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/232.png)

![imagen233](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/233.png)

![imagen234](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/234.png)

![imagen235](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/235.png)

![imagen236](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/236.png)

![imagen237](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/237.png)

---
