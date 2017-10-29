___

# **Instalación Y Configuración DNS Windows.**

Realizamos la Instalación y Configuración de un Servidor DNS en una máquina con Windows Server 2012.

Al haber instalado anteriormente el Active Directory ya tenemos instalado el DNS.

---

# **1. Zona Directa.**

En este apartado tenemos que crear una nueva zona de búsqueda directa en el Servidor.

![imagen01](./images/instalacion_y_configuracion_dns_w2012/01.png)

Creamos una zona de búsqueda directa.

![imagen02](./images/instalacion_y_configuracion_dns_w2012/02.png)

Nos sale el asistente para la nueva zona.

![imagen03](./images/instalacion_y_configuracion_dns_w2012/03.png)

Elegimos el tipo de zona que queremos.

![imagen04](./images/instalacion_y_configuracion_dns_w2012/04.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen05](./images/instalacion_y_configuracion_dns_w2012/05.png)

Le ponemos un nombre a nuestra zona.

![imagen06](./images/instalacion_y_configuracion_dns_w2012/06.png)

Permitimos actualizaciones dinámicas seguras.

![imagen07](./images/instalacion_y_configuracion_dns_w2012/07.png)

Se ha creado la nueva zona.

![imagen08](./images/instalacion_y_configuracion_dns_w2012/08.png)

Ya contamos con otra zona de búsqueda directa.

![imagen09](./images/instalacion_y_configuracion_dns_w2012/09.png)

---

# **2. Zona Inversa.**

En este apartado tenemos que crear una nueva zona de búsqueda inversa para la subred.

![imagen10](./images/instalacion_y_configuracion_dns_w2012/10.png)

Nos sale el asistente para la nueva zona.

![imagen11](./images/instalacion_y_configuracion_dns_w2012/11.png)

Elegimos el tipo de zona que queremos.

![imagen12](./images/instalacion_y_configuracion_dns_w2012/12.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen13](./images/instalacion_y_configuracion_dns_w2012/13.png)

Elegimos la zona de búsqueda inversa para IPv4.

![imagen14](./images/instalacion_y_configuracion_dns_w2012/14.png)

Identificamos la zona de búsqueda inversa escribiendo la Id. de red.

![imagen15](./images/instalacion_y_configuracion_dns_w2012/15.png)

Permitimos actualizaciones dinámicas seguras.

![imagen16](./images/instalacion_y_configuracion_dns_w2012/16.png)

Se ha creado la nueva zona.

![imagen17](./images/instalacion_y_configuracion_dns_w2012/17.png)

Ya contamos con una zona de búsqueda inversa.

![imagen18](./images/instalacion_y_configuracion_dns_w2012/18.png)

---

# **3. Reenviadores.**

Configuramos reenviadores de DNS con un DNS público, por ejemplo 8.8.4.4.

![imagen19](./images/instalacion_y_configuracion_dns_w2012/19.png)

---

# **4. Servidor DNS Caché.**

Configuramos el Servidor para ser Servidor DNS Caché, esto se hace en la configuración estática de red.

![imagen20](./images/instalacion_y_configuracion_dns_w2012/20.png)

Configuramos el Cliente para que su Servidor DNS sea el Servidor Windows 2012.

![imagen21](./images/instalacion_y_configuracion_dns_w2012/21.png)

Comprobamos el funcionamiento como caché DNS de ambas máquinas al acceder a sitios de Internet.

* Desde el Servidor.

![imagen22](./images/instalacion_y_configuracion_dns_w2012/22.png)

* Desde el Cliente.

![imagen23](./images/instalacion_y_configuracion_dns_w2012/23.png)

---

# **5. Servidor DNS Maestro.**

Ahora tenemos que configurar el servidor como DNS Maestro, además de Caché.

![imagen24](./images/instalacion_y_configuracion_dns_w2012/24.png)

En la zona de búsqueda directa añadimos los siguientes registros.

![imagen25](./images/instalacion_y_configuracion_dns_w2012/25.png)

* Un alias para el servidor denominado server.        

![imagen26](./images/instalacion_y_configuracion_dns_w2012/26.png)

* Una impresora con IP fija denominada printer.

![imagen27](./images/instalacion_y_configuracion_dns_w2012/27.png)

* Un servidor de correo denominado correo, asociado a una dirección en mi servidor.

![imagen28](./images/instalacion_y_configuracion_dns_w2012/28.png)

![imagen29](./images/instalacion_y_configuracion_dns_w2012/29.png)

![imagen30](./images/instalacion_y_configuracion_dns_w2012/30.png)

![imagen31](./images/instalacion_y_configuracion_dns_w2012/31.png)

Ya tenemos estos tres registros creados.

![imagen32](./images/instalacion_y_configuracion_dns_w2012/32.png)

Creamos una subzona denominada servicios, un dominio nuevo.

![imagen33](./images/instalacion_y_configuracion_dns_w2012/33.png)

![imagen34](./images/instalacion_y_configuracion_dns_w2012/34.png)

Ahora tenemos que añadir otros registros dentro de la subzona.

![imagen35](./images/instalacion_y_configuracion_dns_w2012/35.png)

Dentro de la subzona demoninada servicios añadimos los siguientes registros.

![imagen36](./images/instalacion_y_configuracion_dns_w2012/36.png)

* Agregamos un servidor ftp.

![imagen37](./images/instalacion_y_configuracion_dns_w2012/37.png)

* Una impresora nueva.

![imagen38](./images/instalacion_y_configuracion_dns_w2012/38.png)

* El Equipo del administrador del sistema.

![imagen39](./images/instalacion_y_configuracion_dns_w2012/39.png)

Finalmente ya tenemos estos tres registros creados.

![imagen40](./images/instalacion_y_configuracion_dns_w2012/40.png)

---

# **6. Comprobaciones.**

Comprobamos que se resuelven los nombres desde la consola del Servidor.

![imagen41](./images/instalacion_y_configuracion_dns_w2012/41.png)

Validamos un cliente en el dominio y comprobamos que el nombre de su equipo aparece en la zona de búsqueda del servidor como un nuevo registro A.

![imagen42](./images/instalacion_y_configuracion_dns_w2012/42.png)

![imagen43](./images/instalacion_y_configuracion_dns_w2012/43.png)

Comprobamos desde la consola del cliente que se resuelven correctamente los nombres dados de alta en el servidor.

![imagen44](./images/instalacion_y_configuracion_dns_w2012/44.png)

Realizamos también desde el cliente, algunas operaciones con nslookup tanto dentro como fuera de nuestra intranet.

* Dentro de nuestra intranet.
![imagen45](./images/instalacion_y_configuracion_dns_w2012/45.png)

* Fuera de nuestra intranet.

![imagen46](./images/instalacion_y_configuracion_dns_w2012/46.png)

---
