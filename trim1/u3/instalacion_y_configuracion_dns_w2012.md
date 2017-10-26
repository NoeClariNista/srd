___

# **Instalación Y Configuración Windows.**

Realizamos la instalación y configuración de un servidor DNS en una máquina con Windows Server 2012. Para esta práctica se piden una serie de acciones de configuración y prueba del funcionamiento del servicio.

---

# **1. Zona Directa.**

Creamos una zona de búsqueda directa en el Servidor.

![imagen01](./images/01.png)

![imagen02](./images/02.png)

![imagen03](./images/03.png)

![imagen04](./images/04.png)

![imagen05](./images/05.png)

![imagen06](./images/06.png)

![imagen07](./images/07.png)

![imagen08](./images/08.png)

![imagen09](./images/09.png)

---

# **2. Zona Inversa.**

Creamos una zona de búsqueda inversa para la subred.

![imagen10](./images/10.png)

![imagen11](./images/11.png)

![imagen12](./images/12.png)

![imagen13](./images/13.png)

![imagen14](./images/14.png)

![imagen15](./images/15.png)

![imagen16](./images/16.png)

![imagen17](./images/17.png)

![imagen18](./images/18.png)

---

# **3. Reenviadores.**

Configuramos reenviadores de DNS con un DNS público, por ejemplo 8.8.4.4.

![imagen19](./images/19.png)

---

# **4. Servidor DNS Caché.**

Configuramos el Servidor para ser Servidor DNS Caché, esto se hace en la configuración estática de red.

![imagen20](./images/20.png)

![imagen21](./images/21.png)

Configuramos el Cliente para que su Servidor DNS sea el Servidor W2012. Comprobamos el funcionamiento como caché DNS de ambas máquinas al acceder a sitios de Internet.

![imagen22](./images/22.png)

![imagen23](./images/23.png)

---

# **5. Servidor DNS Maestro.**

Ahora el servidor como DNS Maestro, además de Caché.

![imagen24](./images/24.png)

En la zona de búsqueda directa añadir los siguientes registros

![imagen25](./images/25.png)

* Un alias para tu servidor denominado server.        

![imagen21](./images/21.png)

* Una impresora con IP fija denominada printer (no hace falta alias).

![imagen21](./images/21.png)

* Un servidor de correo (ficticio) denominado correo, asociado a una dirección en tu servidor.

Crear una subzona denominada servicios (dominio nuevo)

![imagen21](./images/21.png)

* agregar a ésta un servidor ftp (asociado a la misma IP del servidor),

![imagen21](./images/21.png)

* una impresora nueva (con una IP fija)

![imagen21](./images/21.png)

* el equipo del administrador del sistema (también con IP fija).

![imagen21](./images/21.png)


---

# **6. Comprobaciones.**

    Comprobar que se resuelven los nombres desde la consola del servidor.

    Validar un cliente en el dominio y comprobar que el nombre de su equipo aparece en la zona de búsqueda del servidor como un nuevo registro A.

    Comprobar desde la consola del cliente que se resuelven correctamente los nombres dados de alta en el servidor (aunque en algunos casos, si se trata de direcciones ficticias, no se obtenga respuesta).

    Realizar, también desde el cliente, algunas operaciones con nslookup tanto dentro como fuera de nuestra intranet.

---
