___

# **Instalación Y Configuración DNS Windows.**

Realizamos la Instalación y Configuración de un servidor DNS en una máquina con Windows Server 2012.

---

# **1. Zona Directa.**

En este apartado tenemos que crear una nueva zona de búsqueda directa en el Servidor.

![imagen01](./images/01.png)

Creamos una zona de búsqueda directa.

![imagen02](./images/02.png)

Nos sale el asistente para la nueva zona.

![imagen03](./images/03.png)

Elegimos el tipo de zona que queremos.

![imagen04](./images/04.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen05](./images/05.png)

Le ponemos un nombre a nuestra zona.

![imagen06](./images/06.png)

Permitimos actualizaciones dinánmicas seguras.

![imagen07](./images/07.png)

Se ha creado la nueva zona.

![imagen08](./images/08.png)

Ya contamos con otra zona de búsqueda directa.

![imagen09](./images/09.png)

---

# **2. Zona Inversa.**

En este apartado tenemos que crear una nueva zona de búsqueda inversa para la subred.

![imagen10](./images/10.png)

Nos sale el asistente para la nueva zona.

![imagen11](./images/11.png)

Elegimos el tipo de zona que queremos.

![imagen12](./images/12.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen13](./images/13.png)

Elegimos la zona de búsqueda inversa para IPv4.

![imagen14](./images/14.png)

Identificamos la zona de búsqueda inversa escribiendo la id. de red.

![imagen15](./images/15.png)

Permitimos actualizaciones dinánmicas seguras.

![imagen16](./images/16.png)

Se ha creado la nueva zona.

![imagen17](./images/17.png)

Ya contamos con otra zona de búsqueda inversa.

![imagen18](./images/18.png)

---

# **3. Reenviadores.**

Configuramos reenviadores de DNS con un DNS público, por ejemplo 8.8.4.4.

![imagen19](./images/19.png)

---

# **4. Servidor DNS Caché.**

Configuramos el Servidor para ser Servidor DNS Caché, esto se hace en la configuración estática de red.

![imagen20](./images/20.png)

Configuramos el Cliente para que su Servidor DNS sea el Servidor W2012.

![imagen21](./images/21.png)

Comprobamos el funcionamiento como caché DNS de ambas máquinas al acceder a sitios de Internet.

![imagen22](./images/22.png)

![imagen23](./images/23.png)

---

# **5. Servidor DNS Maestro.**

Ahora tenemos que configurar el servidor como DNS Maestro, además de Caché.

![imagen24](./images/24.png)

En la zona de búsqueda directa añadiimos los siguientes registros.

![imagen25](./images/25.png)

* Un alias para el servidor denominado server.        

![imagen26](./images/26.png)

* Una impresora con IP fija denominada printer.

![imagen27](./images/27.png)

* Un servidor de correo denominado correo, asociado a una dirección en mi servidor.

![imagen28](./images/28.png)

![imagen29](./images/29.png)

![imagen30](./images/30.png)

![imagen31](./images/31.png)

![imagen32](./images/32.png)

Crear una subzona denominada servicios (dominio nuevo)

![imagen33](./images/33.png)

![imagen34](./images/34.png)

Ahora tenemos que añadir otros registros dentro de la subzona.

![imagen35](./images/35.png)

Dentro de la subzona demoninada servicios añadimos los siguientes registros.

![imagen36](./images/36.png)

* Agregamos un servidor ftp.

![imagen37](./images/37.png)

* Una impresora nueva.

![imagen38](./images/38.png)

* el Equipo del administrador del sistema.

![imagen39](./images/39.png)

![imagen40](./images/40.png)

---

# **6. Comprobaciones.**

Comprobar que se resuelven los nombres desde la consola del Servidor.

![imagen41](./images/41.png)

Validamos un cliente en el dominio y comprobar que el nombre de su equipo aparece en la zona de búsqueda del servidor como un nuevo registro A.

![imagen42](./images/42.png)

![imagen43](./images/43.png)

Comprobamos desde la consola del cliente que se resuelven correctamente los nombres dados de alta en el servidor.

![imagen44](./images/44.png)

Realizamos también desde el cliente, algunas operaciones con nslookup tanto dentro como fuera de nuestra intranet.

![imagen45](./images/45.png)

---
