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

  * Establecemos como IP todas las asignadas. Limitamos el número de conexiones a 50. Habilitamos el registro en formato W3C, diario y en una carpeta determinada.

    ![imagen015](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/015.png)

    ![imagen016](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/016.png)

  * Configuramos el envío de mensajes dentro de nuestra red local. Aceptamos la conexión al Servidor y la retransmisión de mensajes a todos los equipos menos los que aparecen en la lista, incluimos una IP cualquiera en la lista para impedimos su acceso y retransmisión, en concreto 172.18.20.20.

    ![imagen017](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/017.png)

    ![imagen018](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/018.png)

    ![imagen019](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/019.png)

    ![imagen020](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/020.png)

    ![imagen021](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/021.png)

    [imagen022](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/022.png)

  * Establecemos autenticación anónima.

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

    Ya tenemos este registros creado.

    ![imagen051](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/051.png)

  * Comprobamos la carpetas de correo creados en `C:\Inetpub\mailroot`.

    ![imagen052](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/052.png)

    * En el cliente Windows:

      Comprobamos el acceso al nuevo nombre DNS creado en el Servidor.

        ![imagen053](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/053.png)

      Configuramos el Cliente de correo Live mail agregando dos cuentas de correo cualesquiera. Deberemos especificar el usuario/buzón, la contraseña y el Servidor SMTP.

        ![imagen054](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/054.png)

        ![imagen055](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/055.png)

        ![imagen056](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/056.png)

        ![imagen057](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/057.png)

        ![imagen058](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/058.png)

        ![imagen059](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/059.png) <- recortar.

        ![imagen060](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/060.png)

        ![imagen061](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/061.png)

        ![imagen062](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/062.png)

        ![imagen063](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/063.png)

        ![imagen064](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/064.png)

        ![imagen065](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/065.png)

      Enviamos varios correos desde / hacia las diferentes cuentas y comprobar envío (real o ficticio) y carpetas mailroot. Las carpetas existentes en mailroot alojan mensajes en cola (Queue) y mensajes entregados (Drop).

        ![imagen066](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/066.png)

        ![imagen067](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/067.png) <- revisar correo.

        ![imagen068](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/068.png)

        ![imagen069](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/069.png)

        ![imagen070](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/070.png)

        ![imagen071](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/071.png)

        ![imagen072](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/072.png)

        ![imagen073](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/073.png)

        ![imagen074](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/074.png) <- revisar correo.

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

    * En el Cliente Windows:

      Configuramos las cuentas según los parámetros especificados en el Servidor.

        ![imagen086](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/086.png)

        ![imagen087](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/087.png) <- falta.

        ![imagen088](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/088.png) <-recortar.

        ![imagen089](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/089.png)

        ![imagen090](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/090.png)

        ![imagen091](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/091.png)

        ![imagen092](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/092.png)

        ![imagen093](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/093.png)

        ![imagen094](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/094.png)

        ![imagen095](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/095.png) <- cambiar usuario.

        ![imagen096](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/096.png) <- arreglar.

        ![imagen097](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/097.png) <- recortar.

        ![imagen098](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/098.png)

        ![imagen099](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/099.png)

        ![imagen100](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/100.png)

        ![imagen101](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/101.png)

      Enviamos varios correos desde / hacia las diferentes cuentas y comprobar envío y carpetas mailroot. En este caso sólo tendrán acceso al servidor SMTP cuentas del dominio y correspondientes a usuarios de AD.

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

Queremos configurar un servidor de correo para nuestra red local, para que los usuarios de nuestra red puedan comunicarse por correo electrónico.

En primer lugar, hay que desinstalar el Servicio SMTP de Windows 2012 Server.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Debes descargar e instalar en el Servidor Windows 2012 Server el Servidor de correo hMailServer.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Crea dos dominios denominados srd.edu y asir.edu.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Ejecuta los diagnósticos para ambos dominios y soluciona el error de backup asignando una carpeta para tal fin. Establece copia de seguridad de los mensajes.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Creamos dos cuentas para dos usuarios ficticios en cada uno de los dos dominios. Configuramos las cuentas con diferentes opciones (cuota de disco, auto-reply, forwarding, signature, etc.)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Configuramos el servicio DNS para crear las entradas `mail.srd.edu` y `mail.asir.edu` que apunten a la dirección ip del Servidor Windows 2012.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Realiza todas las opciones de configuración que consideres necesarias y/o convenientes. Consulta para ello los tutoriales cuyos enlaces se proporcionan (opciones de protocolos SMTP, POP e IMAP, rangos de IP, bloqueo de correo entrante, nombre de host, reenvío dominios remotos, blacklists, opciones de logging, etc.) (tutoriales)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Configura en el cliente W10 un Cliente de correo como thunderbird o Live Mail (en los ordenadores clientes) para acceder al Servidor de correo instalado en Windows 2012.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Realiza prueba de envío y recepción de correos entre los diferentes usuarios, comprobando, además de envío y recepción correctas, el efecto de las opciones configuradas en las cuentas.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Crea una lista de distribución empleados asociada al dominio y añade a los dos usuarios de miempresa.com a ella.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

Realiza prueba de envío y recepción de correos por medio de la lista de distribución.

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

---
