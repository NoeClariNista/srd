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

Realizamos la configuración en las propiedades de SMTP:

![imagen14](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/14.png)

  Establecemos como IP todas las asignadas. Limitamos el número de conexiones a 50. Habilitamos el registro en formato W3C, diario y en una carpeta determinada.

    ![imagen15](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/15.png)

    ![imagen16](./images/instalacion_y_configuracion_de_servicios_de_correo_electronico_windows/16.png)

---

    Configuramos el envío de mensajes dentro de nuestra red local: Aceptamos la conexión al Servidor y la retransmisión de mensajes a todos los equipos menos los que aparecen en la lista (incluir una IP cualquiera en la lista para impedir su acceso y retransmisión).



    Establecer autenticación anónima.



    Echar un vistazo al resto de opciones de configuración del servidor. Aplicar cambios y reiniciar servicio.



    Comprobar la existencia del dominio AD predeterminado. Crea un dominio de tipo alias para disponer de cuentas en otro dominio.



    Comprueba carpetas de correo creados en C:\Inetpub\mailroot.



    * En el cliente Windows:

        Comprobar acceso al nuevo nombre DNS creado en el servidor.

        Configurar el cliente de correo Live mail agregando dos cuentas de correo cualesquiera (usuarios AD -dominio- y no AD). Se deberá especificar: usuario / buzón, contraseña,  servidor SMTP.

        Enviar varios correos desde / hacia las diferentes cuentas y comprobar envío (real o ficticio) y carpetas mailroot. Las carpetas existentes en mailroot alojan mensajes en cola (Queue), mensajes para destinatarios desconocidos (Badmail) y mensajes entregados (Drop).

    Nueva configuración de servicio SMTP a través del administrador de aplicaciones (IIS) 6.0. Establecer autenticación básica de Windows. Probar diferentes configuraciones de dominio predeterminado, cifrado TLS, etc.

    * En el cliente Windows:

        Configurar las cuentas según los parámetros especificados en el servidor. Enviar varios correos desde / hacia las diferentes cuentas y comprobar envío y carpetas mailroot. En este caso sólo tendrán acceso al servidor SMTP cuentas del dominio y correspondientes a usuarios de AD.

---
