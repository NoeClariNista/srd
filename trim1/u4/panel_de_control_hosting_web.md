___

# **Panel De Control Hosting Web.**

---

En esta práctica voy a utilizar el Webmin en la instalación de un panel de control para servicio de hosting web.

---

# **1. Descarga De Webmin.**

Vamos a ir a la página oficial de [Webmin](http://www.webmin.com/).

![imagen01](./images/panel_de_control_hosting_web/01.png)

Luego vamos a Download y nos descargamos por comandos Webmin con la dirección que nos aparece en la página, la versión para Ubuntu.

![imagen02](./images/panel_de_control_hosting_web/02.png)

![imagen03](./images/panel_de_control_hosting_web/03.png)

Confirmamos que se ha descargado bien.

![imagen04](./images/panel_de_control_hosting_web/04.png)

---

# **2. Instalación De Webmin.**

Instalamos Webmin.

![imagen05](./images/panel_de_control_hosting_web/05.png)

Nos da un error y hacemos la siguiente instalación.

![imagen06](./images/panel_de_control_hosting_web/06.png)

---

# **3. Configuración De Webmin.**

Introducimos la dirección 172.18.20.41:10000. Nos da un error de seguridad.

![imagen07](./images/panel_de_control_hosting_web/07.png)

Añadimos una excepción de seguridad.

![imagen08](./images/panel_de_control_hosting_web/08.png)

Volvemos a entrar y nos sale lo siguiente. Introducimos nuestro usuario y contraseña.

![imagen09](./images/panel_de_control_hosting_web/09.png)

Ya estamos dentro de Webmin.

![imagen10](./images/panel_de_control_hosting_web/10.png)

---

# **4. Gestiones.**

Tenemos que hacer las gestiones dentro del Server.

![imagen11](./images/panel_de_control_hosting_web/11.png)

## **4.1. Gestión De Apache.**

En la primera pestaña del Apache Webserver podemos ver lo siguiente.

![imagen12](./images/panel_de_control_hosting_web/12.png)

En la segunda pestaña vemos lo siguiente.

![imagen13](./images/panel_de_control_hosting_web/13.png)

En la última pestaña vemos lo siguiente.

![imagen14](./images/panel_de_control_hosting_web/14.png)

## **4.2. Gestión De BIND DNS Server.**

En el BIND DNS Server vemos lo siguiente. Donde se encuentra nuestro DNS de empresa20.com.

![imagen15](./images/panel_de_control_hosting_web/15.png)

Entramos dentro de nuestro DNS existente y vemos lo siguiente.

![imagen16](./images/panel_de_control_hosting_web/16.png)

También podemos ver todos los alias y hosts que tenemos creados, para ello vamos a All Record Types.

![imagen17](./images/panel_de_control_hosting_web/17.png)

![imagen18](./images/panel_de_control_hosting_web/18.png)

## **4.3. Gestión De MySQL.**

En MySQL Database Server podemos ver que tenemos que entrar como root y con su contraseña.

![imagen19](./images/panel_de_control_hosting_web/19.png)

Aquí vemos las base de datos creadas y más datos de cada una.

![imagen20](./images/panel_de_control_hosting_web/20.png)

---
