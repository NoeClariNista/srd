___

# **Instalación Y Configuración De Un Servidor De Mensajería Instantánea En Windows.**

---

Comprobamos que en el Servidor Windows 2012 están instalados y funcionan correctamente IIS, PHP, MySQL y phpMyAdmin.

![imagen01](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/01.png)

Descargamos e instalamos el Servidor de mensajería instantánea OpenFire para Windows.

![imagen02](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/02.png)

![imagen03](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/03.png)

![imagen04](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/04.png)

![imagen05](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/05.png)

![imagen06](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/06.png)

![imagen07](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/07.png)

![imagen08](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/08.png)

![imagen09](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/09.png)

Iniciamos (Start) el Servidor de mensajería Openfire.

![imagen10](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/10.png)

Creamos una base de datos en blanco en MySqQL a través de phpMyAdmin y recordamos el nombre de la BD, así como el usuario y la contraseña con privilegios.

![imagen11](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/11.png)

![imagen12](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/12.png)

![imagen13](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/13.png)

![imagen14](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/14.png)

Ejecutamos el script de instalación de Openfire desde un navegador web del Servidor, mediante la URL `http://127.0.0.1:9090`.

![imagen15](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/15.png)

Seguimos las instrucciones del documento PDF de Servicio de Mensajería en Windows para seleccionar las distintas opciones de instalación y configuración de Openfire.

![imagen16](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/16.png)

![imagen17](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/17.png)

![imagen18](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/18.png)

![imagen19](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/19.png)

En la primera pantalla de “Seteos de Perfil” seleccionamos la opción “Por Defecto” en lugar del “Servidor de Directorio (LDAP)” que se recomienda en el tutorial de instalación.

![imagen20](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/20.png)

![imagen21](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/21.png)

Una vez completada la instalación, accedemos a la consola de administración de Openfire con el usuario administrador creado. Comprobamos este acceso tanto desde el Servidor como desde una máquina Cliente.

![imagen22](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/22.png)

* Desde el Servidor.

  ![imagen23](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/23.png)

  ![imagen24](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/24.png)

* Desde el Cliente.

  ![imagen25](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/25.png)

  ![imagen26](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/26.png)

Una vez instalado el Servidor OpenFire, vamos a descargarnos e instalar un Cliente de Mensajería.

  Descargamos el Cliente de mensajería Spark.

  ![imagen27](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/27.png)

  Instalamos Spark en nuestro Servidor Windows Server.

  ![imagen28](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/28.png)

  ![imagen29](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/29.png)

  ![imagen30](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/30.png)

  ![imagen31](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/31.png)

  ![imagen32](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/32.png)

  ![imagen33](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/33.png)

  Instalamos también Spark en nuestro Cliente Windows 10.

  ![imagen34](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/34.png)

  ![imagen35](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/35.png)

  ![imagen36](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/36.png)

  ![imagen37](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/37.png)

  ![imagen38](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/38.png)

  ![imagen39](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/39.png)

Ahora vamos a crear dos nuevos usuarios en OpenFire (además del Administrador) para poder mantener una conversación entre Cliente y Servidor.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Ejecutamos Spark tanto en el Cliente como en el Servidor, validamos en cada uno de ellos con un usuario diferente de los que hemos creado y mantenemos conversaciones entre ambas máquinas usando los Clientes de mensajería. Para ello debemos investigar como invitar usuarios, crear cuartos de conferencia, iniciar conversaciones, iniciar conferencias, transferir archivos y capturas de pantalla, etc. Comprobamos e informamos acerca de estas y otras opciones de configuración tanto desde Sparks como desde OpenFire.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Instalamos, probamos e informamos FastPath WebChat (documento pdf) o SparkWeb de OpenFire.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

---
