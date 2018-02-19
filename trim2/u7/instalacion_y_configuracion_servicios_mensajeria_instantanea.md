___

# **Instalación Y Configuración De Un Servidor De Mensajería Instantánea En Windows.**

---

Comprobamos que en el Servidor Windows 2012 están instalados y funcionan correctamente el IIS, el PHP, el MySQL y el phpMyAdmin.

![imagen001](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/001.png)

Descargamos e instalamos el Servidor de mensajería instantánea OpenFire para Windows.

![imagen002](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/002.png)

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen003](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/003.png)

![imagen004](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/004.png)

![imagen005](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/005.png)

![imagen006](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/006.png)

![imagen007](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/007.png)

![imagen008](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/008.png)

Iniciamos (Start) el Servidor de mensajería Openfire.

![imagen009](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/009.png)

Creamos una base de datos en blanco en MySqQL a través de phpMyAdmin y recordamos el nombre de la BD, así como el usuario y la contraseña con privilegios.

![imagen010](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/010.png)

![imagen011](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/011.png)

![imagen012](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/012.png)

![imagen013](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/013.png)

Ejecutamos el script de instalación de Openfire desde un navegador web del Servidor, mediante la URL `http://127.0.0.1:9090`.

![imagen014](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/014.png)

Seleccionamos las siguientes opciones de instalación y configuración de Openfire.

![imagen015](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/015.png)

![imagen016](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/016.png)

![imagen017](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/017.png)

![imagen018](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/018.png)

En la pantalla de “Configuración de Perfil” seleccionamos la opción “Por Defecto”.

![imagen019](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/019.png)

![imagen020](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/020.png)

![imagen021](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/021.png)

Una vez completada la instalación, accedemos a la consola de administración de Openfire con el usuario administrador creado. Comprobamos este acceso tanto desde el Servidor como desde una máquina Cliente.

* Desde el Servidor.

  ![imagen022](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/022.png)

  ![imagen023](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/023.png)

* Desde el Cliente.

  ![imagen024](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/024.png)

  ![imagen025](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/025.png)

Una vez instalado el Servidor OpenFire, vamos a descargarnos e instalar un Cliente de Mensajería.

  Descargamos el Cliente de mensajería Spark.

  ![imagen026](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/026.png)

  Instalamos Spark en nuestro Servidor Windows Server.

  Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

  ![imagen027](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/027.png)

  ![imagen028](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/028.png)

  ![imagen029](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/029.png)

  ![imagen030](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/030.png)

  ![imagen031](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/031.png)

  ![imagen032](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/032.png)

  Instalamos también Spark en nuestro Cliente Windows 10.

  Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

  ![imagen033](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/033.png)

  ![imagen034](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/034.png)

  ![imagen035](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/035.png)

  ![imagen036](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/036.png)

  ![imagen037](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/037.png)

  ![imagen038](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/038.png)

Ahora vamos a crear dos nuevos usuarios en OpenFire (además del Administrador) para poder mantener una conversación entre Cliente y Servidor.

![imagen039](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/039.png)

![imagen040](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/040.png)

![imagen041](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/041.png)

![imagen042](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/042.png)

![imagen043](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/043.png)

![imagen044](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/044.png)

![imagen045](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/045.png)

Ejecutamos Spark tanto en el Cliente como en el Servidor, validamos en cada uno de ellos con un usuario diferente de los que hemos creado.

* En el Servidor.

![imagen046](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/046.png)

![imagen047](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/047.png)

![imagen048](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/048.png)

* En el Cliente.

![imagen049](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/049.png)

![imagen050](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/050.png)

![imagen051](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/051.png)

Lo primero que tenemos que hacer es invitar usuarios. Para ello hacemos lo siguiente.

![imagen052](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/052.png)

![imagen053](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/053.png)

![imagen054](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/054.png)

![imagen055](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/055.png)

![imagen056](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/056.png)

![imagen057](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/057.png)

![imagen058](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/058.png)

Creamos cuartos de conferencia e iniciamos conferencias.

![imagen059](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/059.png)

![imagen060](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/060.png)

![imagen061](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/061.png)

![imagen062](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/062.png)

![imagen063](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/063.png)

![imagen064](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/064.png)

![imagen065](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/065.png)

![imagen066](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/066.png)

![imagen067](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/067.png)

![imagen068](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/068.png)

Iniciamos conversaciones entre ambas máquinas usando los Clientes de mensajería.

![imagen069](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/069.png)

![imagen070](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/070.png)

Transferimos archivos entre ambas máquinas usando los Clientes de mensajería.

![imagen071](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/071.png)

![imagen072](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/072.png)

![imagen073](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/073.png)

![imagen074](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/074.png)

![imagen075](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/075.png)

![imagen076](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/076.png)

Realizamos una discusión desde Spark entre ambos Clientes de mensajería.

![imagen077](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/077.png)

![imagen078](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/078.png)

![imagen079](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/079.png)

![imagen080](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/080.png)

![imagen081](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/081.png)

![imagen082](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/082.png)

Revisamos las opciones que tenemos desde OpenFire.

![imagen083](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/083.png)

![imagen084](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/084.png)

Realizamos una conferencia desde OpenFire.

![imagen085](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/085.png)

![imagen086](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/086.png)

![imagen087](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/087.png)

![imagen088](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/088.png)

![imagen089](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/089.png)

![imagen090](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/090.png)

![imagen091](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/091.png)

![imagen092](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/092.png)

![imagen093](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/093.png)

![imagen094](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/094.png)

Instalamos, probamos e informamos SparkWeb de OpenFire.

![imagen095](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/095.png)

![imagen096](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/096.png)

![imagen097](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/097.png)

![imagen098](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/098.png)

![imagen099](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/099.png)

![imagen100](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/100.png)

![imagen101](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/101.png)

![imagen102](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/102.png)

![imagen103](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/103.png)

![imagen104](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/104.png)

![imagen105](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/105.png)

![imagen106](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/106.png)

---
