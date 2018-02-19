___

# **Instalación Y Configuración De Un Servidor De Mensajería Instantánea En Windows.**

---

Comprobamos que en el Servidor Windows 2012 están instalados y funcionan correctamente el IIS, el PHP, el MySQL y el phpMyAdmin.

![imagen01](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/01.png)

Descargamos e instalamos el Servidor de mensajería instantánea OpenFire para Windows.

![imagen02](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/02.png)

Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

![imagen03](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/03.png)

![imagen04](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/04.png)

![imagen05](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/05.png)

![imagen06](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/06.png)

![imagen07](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/07.png)

![imagen08](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/08.png)

Iniciamos (Start) el Servidor de mensajería Openfire.

![imagen09](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/09.png)

Creamos una base de datos en blanco en MySqQL a través de phpMyAdmin y recordamos el nombre de la BD, así como el usuario y la contraseña con privilegios.

![imagen10](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/10.png)

![imagen11](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/11.png)

![imagen12](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/12.png)

![imagen13](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/13.png)

Ejecutamos el script de instalación de Openfire desde un navegador web del Servidor, mediante la URL `http://127.0.0.1:9090`.

![imagen14](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/14.png)

Seleccionamos las siguientes opciones de instalación y configuración de Openfire.

![imagen15](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/15.png)

![imagen16](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/16.png)

![imagen17](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/17.png)

![imagen18](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/18.png)

En la pantalla de “Configuración de Perfil” seleccionamos la opción “Por Defecto”.

![imagen19](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/19.png)

![imagen20](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/20.png)

![imagen21](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/21.png)

Una vez completada la instalación, accedemos a la consola de administración de Openfire con el usuario administrador creado. Comprobamos este acceso tanto desde el Servidor como desde una máquina Cliente.

* Desde el Servidor.

  ![imagen22](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/22.png)

  ![imagen23](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/23.png)

* Desde el Cliente.

  ![imagen24](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/24.png)

  ![imagen25](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/25.png)

Una vez instalado el Servidor OpenFire, vamos a descargarnos e instalar un Cliente de Mensajería.

  Descargamos el Cliente de mensajería Spark.

  ![imagen26](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/26.png)

  Instalamos Spark en nuestro Servidor Windows Server.

  Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

  ![imagen27](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/27.png)

  ![imagen28](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/28.png)

  ![imagen29](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/29.png)

  ![imagen30](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/30.png)

  ![imagen31](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/31.png)

  ![imagen32](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/32.png)

  Instalamos también Spark en nuestro Cliente Windows 10.

  Los pasos de la instalación los realizamos como se pueden ver en las imágenes.

  ![imagen33](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/33.png)

  ![imagen34](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/34.png)

  ![imagen35](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/35.png)

  ![imagen36](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/36.png)

  ![imagen37](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/37.png)

  ![imagen38](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/38.png)

Ahora vamos a crear dos nuevos usuarios en OpenFire (además del Administrador) para poder mantener una conversación entre Cliente y Servidor.

![imagen39](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/39.png)

![imagen40](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/40.png)

![imagen41](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/41.png)

![imagen42](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/42.png)

![imagen43](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/43.png)

![imagen44](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/44.png)

![imagen45](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/45.png)

Ejecutamos Spark tanto en el Cliente como en el Servidor, validamos en cada uno de ellos con un usuario diferente de los que hemos creado.

* En el Servidor.

![imagen46](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/46.png)

![imagen47](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/47.png)

![imagen48](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/48.png)

* En el Cliente.

![imagen49](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/49.png)

![imagen50](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/50.png)

![imagen51](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/51.png)

Lo primero que tenemos que hacer es invitar usuarios. Para ello hacemos lo siguiente.

![imagen52](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/52.png)

![imagen53](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/53.png)

![imagen54](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/54.png)

![imagen55](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/55.png)

![imagen56](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/56.png)

![imagen57](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/57.png)

![imagen58](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/58.png)

Creamos cuartos de conferencia e iniciamos conferencias.

![imagen59](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/59.png)

![imagen60](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/60.png)

![imagen61](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/61.png)

![imagen62](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/62.png)

![imagen63](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/63.png)

![imagen64](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/64.png)

![imagen65](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/65.png)

![imagen66](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/66.png)

![imagen67](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/67.png)

![imagen68](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/68.png)

Iniciamos conversaciones entre ambas máquinas usando los Clientes de mensajería.

![imagen69](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/69.png)

![imagen70](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/70.png)

Transferimos archivos entre ambas máquinas usando los Clientes de mensajería.

![imagen71](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/71.png)

![imagen72](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/72.png)

![imagen73](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/73.png)

![imagen74](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/74.png)

![imagen75](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/75.png)

![imagen76](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/76.png)

Realizamos una discusión desde Spark entre ambos Clientes de mensajería.

![imagen77](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/77.png)

![imagen78](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/78.png)

![imagen79](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/79.png)

![imagen80](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/80.png)

![imagen81](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/81.png)

![imagen82](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/82.png)

Revisamos las opciones que tenemos desde OpenFire.

![imagen83](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/83.png)

![imagen84](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/84.png)

Realizamos una conferencia desde OpenFire.

![imagen85](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/85.png)

![imagen86](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/86.png)

![imagen87](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/87.png)

![imagen88](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/88.png)

![imagen89](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/89.png)

![imagen90](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/90.png)

![imagen91](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/91.png)

![imagen92](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/92.png)

![imagen93](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/93.png)

![imagen94](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/94.png)

Instalamos, probamos e informamos SparkWeb de OpenFire.

![imagen95](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/95.png)

![imagen96](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/96.png)

![imagen97](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/97.png)

![imagen98](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/98.png)

![imagen99](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/99.png)

![imagen100](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/100.png)

![imagen101](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/101.png)

![imagen102](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/102.png)

![imagen103](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/103.png)

![imagen104](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/104.png)

![imagen105](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/105.png)

![imagen106](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/106.png)

---
