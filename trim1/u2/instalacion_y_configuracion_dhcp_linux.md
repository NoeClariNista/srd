___

# **Instalación Y Configuración DHCP Linux.**

___

# **1. Introducción.**

Vamos a crear un manual de instalación y configuración de un servidor DHCP en una máquina con Linux, en esta instalación en Ubuntu. También utilizaremos otra máquina con Linux, otro Ubuntu, para hacer que utilice el servidor DHCP.

Durante esta instalación y configuración hay que tener en cuenta que el servidor no debe estar abierto a la red, es decir, hay que configurar el adaptador en red interna para no provocar conflictos de direcciones.

---

# **2. Instalación Del Servicio DHCP En Linux.**

Instalamos el servicio DHCP en Ubuntu Linux.

![imagen01](./images/instalacion_y_configuracion_dhcp_linux/01.png)

![imagen02](./images/instalacion_y_configuracion_dhcp_linux/02.png)

---

# **3. Configuración Del Servicio DHCP.**

Configuramos el servicio DHCP para ello tenemos que modificar el archivo /etc/dhcp/dhcpd.conf.

![imagen03](./images/instalacion_y_configuracion_dhcp_linux/03.png)

Dentro de este archivo creamos una ámbito para el servicio DHCP. Para ello ponemos unas direcciones IP que considero convenientes. Configuro la puerta de enlace, los servidores DNS a suministrar a los clientes. También configuramos un rango de direcciones IP para suministrar a los clientes.

![imagen04](./images/instalacion_y_configuracion_dhcp_linux/04.png)

Ahora tenemos que iniciar el servicio DHCP y ver su estado.

![imagen05](./images/instalacion_y_configuracion_dhcp_linux/05.png)
___

# **4. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello ponemos la máquina Cliente en DHCP y ponemos el comando ifconfig.

![imagen06](./images/instalacion_y_configuracion_dhcp_linux/06.png)

![imagen07](./images/instalacion_y_configuracion_dhcp_linux/07.png)

---

# **5. Reserva.**

Luego creamos una reserva de dirección asociada a un equipo específico (MAC). Para ello lo creamos dentro de donde tenemos el ámbito.

![imagen08](./images/instalacion_y_configuracion_dhcp_linux/08.png)

Dentro de este archivo creamos una reserva para nuestro cliente. Para ello ponemos la dirección MAC de mi cliente, una dirección IP que considero conveniente y configuro la puerta de enlace.

![imagen09](./images/instalacion_y_configuracion_dhcp_linux/09.png)

Ahora tenemos que reiniciar el servicio DHCP y ver su estado.

![imagen10](./images/instalacion_y_configuracion_dhcp_linux/10.png)

___

# **6. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello ponemos el comando ifconfig.

![imagen11](./images/instalacion_y_configuracion_dhcp_linux/11.png)
___

# **6. Otras Opciones.**

Configuramos algunas opciones de servidor además de las habituales. Por ejemplo, el tiempo por defecto que tendran las direcciones IP y el máximo tiempo que tendra las direcciones IP.

![imagen12](./images/instalacion_y_configuracion_dhcp_linux/12.png)

![imagen13](./images/instalacion_y_configuracion_dhcp_linux/13.png)
___

# **7. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello ponemos el comando ifconfig.

![imagen14](./images/instalacion_y_configuracion_dhcp_linux/14.png)

---
