___

# **Práctica Servicio SMTP Windows 2012 Server.**

---

## **Instalación Y Configuración De Un Servidor De Correo SMTP.**

Instalamos el Servicio SMTP en Windows 2012 Server utilizando Asistente.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen01](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/01.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen02](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/02.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen03](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/03.png)

![imagen04](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/04.png)

![imagen05](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/05.png)

![imagen06](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/06.png)

![imagen07](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/07.png)

![imagen08](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/08.png)

![imagen09](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/09.png)

Finalmente terminamos la instalación del Servicio SMTP en Windows 2012 Server.

![imagen10](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/10.png)

Configuración de Servicio SMTP a través del Administrador de aplicaciones (IIS) 6.0.

Lo que tenemos que hacer es ir a Administrador del Servidor.

![imagen11](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/11.png)

Luego tenemos que ir a Herramientas y vamos a Administrador de Internet Information Services (IIS) 6.0.

![imagen12](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/12.png)

![imagen13](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/13.png)

Realizamos la configuración en las propiedades de SMTP.

![imagen14](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/14.png)

  * Establecemos como IP todas las asignadas. Limitamos el número de conexiones a 50. Habilitamos el registro en formato W3C, diario y en una carpeta determinada.

    ![imagen15](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/15.png)

    ![imagen16](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/16.png)

  * Configuramos el envío de mensajes dentro de nuestra red local. Aceptamos la conexión al Servidor y la retransmisión de mensajes a todos los equipos menos los que aparecen en la lista, incluimos una IP cualquiera en la lista para impedimos su acceso y retransmisión, en concreto 172.18.20.20.

    ![imagen17](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/17.png)

    ![imagen18](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/18.png)

    ![imagen19](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/19.png)

    ![imagen20](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/20.png)

    ![imagen21](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/21.png)

    [imagen22](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/22.png)

  * Establecemos autenticación anónima.

    ![imagen23](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/22.png)

    ![imagen24](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/22.png)

  * Echamos un vistazo al resto de opciones de configuración del servidor.

    ![imagen25](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/25.png)

    ![imagen26](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/26.png)

    ![imagen27](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/27.png)

    ![imagen28](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/28.png)

  * Aplicamos cambios y reiniciamos el Servicio.

    ![imagen29](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/29.png)

    ![imagen30](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/30.png)

    ![imagen31](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/31.png)

    ![imagen32](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/32.png)

  * Comprobamos la existencia del dominio AD predeterminado. Creamos un dominio de tipo alias para disponer de cuentas en otro dominio.

    ![imagen33](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/33.png)

    ![imagen34](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/34.png)

    ![imagen35](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/35.png)

    ![imagen36](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/36.png)

    ![imagen37](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/37.png)

  * Creamos un nuevo DNS.

    ![imagen38](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/38.png)

    ![imagen39](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/39.png)

    ![imagen40](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/40.png)

    ![imagen41](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/41.png)

    ![imagen42](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/42.png)

    ![imagen43](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/43.png)

    ![imagen44](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/44.png)

    ![imagen45](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/45.png)

    ![imagen46](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/46.png)

    ![imagen47](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/47.png)

    ![imagen48](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/48.png)

    ![imagen49](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/49.png)

    ![imagen50](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/50.png)

    ![imagen51](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/51.png)

  * Comprobamos carpetas de correo creados en C:\Inetpub\mailroot.

    ![imagen52](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/52.png)

    * En el cliente Windows:

      Comprobar acceso al nuevo nombre DNS creado en el Servidor.

        ![imagen53](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/53.png)

      Configurar el Cliente de correo Live mail agregando dos cuentas de correo cualesquiera (usuarios AD -dominio- y no AD). Se deberá especificar: usuario / buzón, contraseña,  servidor SMTP.

        ![imagen54](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/54.png)

        ![imagen55](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/55.png)

        ![imagen56](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/56.png)

        ![imagen57](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/57.png)

        ![imagen58](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/58.png)

        ![imagen59](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/59.png)

        ![imagen60](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/60.png)

        ![imagen61](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/61.png)

        ![imagen62](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/62.png)

        ![imagen63](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/63.png)

        ![imagen64](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/64.png)

      Enviar varios correos desde / hacia las diferentes cuentas y comprobar envío (real o ficticio) y carpetas mailroot. Las carpetas existentes en mailroot alojan mensajes en cola (Queue), mensajes para destinatarios desconocidos (Badmail) y mensajes entregados (Drop).

        ![imagen65](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/65.png)

        ![imagen66](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/66.png)

        ![imagen67](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/67.png)

        ![imagen68](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/68.png)

        ![imagen69](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/69.png)

        ![imagen70](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/70.png)

        ![imagen71](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/71.png)

        ![imagen72](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/72.png)

        ![imagen73](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/73.png)

        ![imagen74](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/74.png)

        ![imagen75](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/75.png)

    * En el Servidor.

      Nueva configuración de servicio SMTP a través del administrador de aplicaciones (IIS) 6.0.

        ![imagen76](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/76.png)

        ![imagen77](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/77.png)

        ![imagen78](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/78.png)

        ![imagen79](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/79.png)

        ![imagen80](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/80.png)

      Establecer autenticación básica de Windows.

        ![imagen81](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/81.png)

        ![imagen82](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/82.png)

      Probar diferentes configuraciones de dominio predeterminado, por ejemplo, cifrado TLS.

        ![imagen83](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/83.png)

        ![imagen84](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/84.png)

    * En el Cliente Windows:

      Configuramos las cuentas según los parámetros especificados en el Servidor.

        ![imagen85](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/85.png)

        ![imagen86](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/86.png)

        ![imagen87](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/87.png)

        ![imagen88](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/88.png)

        ![imagen89](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/89.png)

        ![imagen90](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/90.png)

        ![imagen91](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/91.png)

        ![imagen92](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/92.png)

        ![imagen93](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/93.png)

        ![imagen94](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/94.png)

        ![imagen95](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/95.png)

        ![imagen96](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/96.png)

        ![imagen97](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/97.png)

      Enviamos varios correos desde / hacia las diferentes cuentas y comprobar envío y carpetas mailroot. En este caso sólo tendrán acceso al servidor SMTP cuentas del dominio y correspondientes a usuarios de AD.

        ![imagen98](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/98.png)

        ![imagen99](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/99.png)

        ![imagen100](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/100.png)

        ![imagen101](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/101.png)

        ![imagen102](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/102.png)

        ![imagen103](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/103.png)

        ![imagen104](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/104.png)

        ![imagen105](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/105.png)

---
