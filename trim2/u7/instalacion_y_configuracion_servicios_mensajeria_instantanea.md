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

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Creamos una base de datos en blanco en MySqQL a través de phpMyAdmin y recordamos el nombre de la BD, así como el usuario y la contraseña con privilegios.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Ejecutamos el script de instalación de Openfire desde un navegador web del Servidor, mediante la URL http://127.0.0.1:9090.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Seguimos las instrucciones del documento PDF de Servicio de Mensajería en Windows para seleccionar las distintas opciones de instalación y configuración de Openfire.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

En la primera pantalla de “Seteos de Perfil” seleccionamos la opción “Por Defecto” en lugar del “Servidor de Directorio (LDAP)” que se recomienda en el tutorial de instalación.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Una vez completada la instalación, accedemos a la consola de administración de Openfire con el usuario administrador creado. Comprobamos este acceso tanto desde el Servidor como desde una máquina Cliente.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Una vez instalado el Servidor OpenFire, vamos a descargarnos e instalar un Cliente de Mensajería.

  Descargamos el Cliente de mensajería Spark.

  ![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

  Instalamos Spark en nuestro Servidor Windows Server.

  ![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

  Instalamos también Spark en nuestro Cliente Windows 10.

  ![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Ahora vamos a crear dos nuevos usuarios en OpenFire (además del Administrador) para poder mantener una conversación entre Cliente y Servidor.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Ejecutamos Spark tanto en el Cliente como en el Servidor, validamos en cada uno de ellos con un usuario diferente de los que hemos creado y mantenemos conversaciones entre ambas máquinas usando los Clientes de mensajería. Para ello debemos investigar como invitar usuarios, crear cuartos de conferencia, iniciar conversaciones, iniciar conferencias, transferir archivos y capturas de pantalla, etc. Comprobamos e informamos acerca de estas y otras opciones de configuración tanto desde Sparks como desde OpenFire.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

Instalamos, probamos e informamos FastPath WebChat (documento pdf) o SparkWeb de OpenFire.

![imagen00](./images/instalacion_y_configuracion_servicios_mensajeria_instantanea/00.png)

---
