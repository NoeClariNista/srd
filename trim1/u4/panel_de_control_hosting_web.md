___

# **Panel De Control Hosting Web.**

---

En esta práctica vamos a utilizar el Webmin en la instalación y la configuración de un Panel de Control para servicio de hosting web en un Servidor.

---

# **1. Descarga De Webmin.**

Vamos a ir a la página oficial de [Webmin](http://www.webmin.com/).

![imagen01](./images/panel_de_control_hosting_web/01.png)

Luego vamos a Download y nos descargamos por comandos Webmin con la dirección que nos aparece en la página, la versión para Ubuntu.

![imagen02](./images/panel_de_control_hosting_web/02.png)

![imagen03](./images/panel_de_control_hosting_web/03.png)

Confirmamos que se ha descargado bien Webmin.

![imagen04](./images/panel_de_control_hosting_web/04.png)

---

# **2. Instalación De Webmin.**

Instalamos Webmin.

![imagen05](./images/panel_de_control_hosting_web/05.png)

![imagen06](./images/panel_de_control_hosting_web/06.png)

---

# **3. Configuración De Webmin.**

Introducimos en nuestro navegador la dirección `https://172.18.20.41:10000`.

![imagen07](./images/panel_de_control_hosting_web/07.png)

Nos da un error de seguridad por tener un certificado autofirmado entonces añadimos una excepción de seguridad.

![imagen08](./images/panel_de_control_hosting_web/08.png)

Volvemos a entrar y nos sale para introducir nuestro usuario y nuestra contraseña.

![imagen09](./images/panel_de_control_hosting_web/09.png)

Con esto ya hemos podido acceder a Webmin.

![imagen10](./images/panel_de_control_hosting_web/10.png)

---

# **4. Gestiones.**

Tenemos que hacer las gestiones dentro de la pestaña Server.

![imagen11](./images/panel_de_control_hosting_web/11.png)

## **4.1. Gestión De Apache.**

Vamos a Apache Webserver.

En la primera pestaña del Apache Webserver podemos ver la configuración global.

![imagen12](./images/panel_de_control_hosting_web/12.png)

En la segunda pestaña podemos ver los virtual host que ya tenemos creados en nuestro Servidor.

![imagen13](./images/panel_de_control_hosting_web/13.png)

En la última pestaña podemos ver donde podemos crear nuevos virtual hosts.

![imagen14](./images/panel_de_control_hosting_web/14.png)

## **4.2. Gestión De BIND DNS Server.**

Vamos a BIND DNS Server.

Podemos ver donde modificar las opciones globales del Servidor. En este apartado podemos ver el DNS de empresa20.com.

![imagen15](./images/panel_de_control_hosting_web/15.png)

Entramos dentro de nuestro DNS existente.

![imagen16](./images/panel_de_control_hosting_web/16.png)

Dentro de nuestro DNS podemos ver todos los alias y hosts que tenemos creados, para ello vamos a All Record Types.

![imagen17](./images/panel_de_control_hosting_web/17.png)

![imagen18](./images/panel_de_control_hosting_web/18.png)

## **4.3. Gestión De MySQL.**

Vamos a MySQL Database Server.

Para poder acceder al Servidor MySQL tenemos que entrar como root y poner una contraseña para este usuario.

![imagen19](./images/panel_de_control_hosting_web/19.png)

Aquí vemos las base de datos creadas y más datos de cada una.

![imagen20](./images/panel_de_control_hosting_web/20.png)

---
