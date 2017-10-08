___

# **Instalación Y Configuración DHCP Linux.**

___

# **1. Introducción.**

Vamos a crear un manual de instalación y configuración de un servidor DHCP en una máquina con Linux, en esta instalación utilizaremos Ubuntu (Server). También utilizaremos otra máquina con Linux, otro Ubuntu (Cliente), para hacer que utilice el servidor DHCP.

Durante esta instalación y configuración hay que tener en cuenta que el servidor no debe estar abierto a la red, es decir, hay que configurar el adaptador en red interna para no provocar conflictos de direcciones.

---

# **2. Instalación Del Servicio DHCP En Linux.**

Instalamos el servicio DHCP en Ubuntu.

![imagen01](./images/instalacion_y_configuracion_dhcp_linux/01.png)

---

# **3. Configuración Del Servicio DHCP.**

Configuramos el servicio DHCP, para ello tenemos que modificar el archivo /etc/dhcp/dhcpd.conf.

![imagen02](./images/instalacion_y_configuracion_dhcp_linux/02.png)

Dentro de este archivo creamos un ámbito nuevo para el servicio DHCP. Ponemos una subred con su dirección y su máscara, las cuales he considerado convenientes. Configuramos la puerta de enlace y los servidores DNS a suministrar a los clientes. También configuramos un rango de direcciones IP para suministrar a los clientes.

![imagen03](./images/instalacion_y_configuracion_dhcp_linux/03.png)

Ahora tenemos que iniciar el servicio DHCP y ver su estado.

![imagen04](./images/instalacion_y_configuracion_dhcp_linux/04.png)

___

# **4. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello ponemos la máquina Cliente en DHCP y en la consola ponemos el comando ifconfig.

![imagen05](./images/instalacion_y_configuracion_dhcp_linux/05.png)

![imagen06](./images/instalacion_y_configuracion_dhcp_linux/06.png)

---

# **5. Reserva.**

Creamos una reserva de una dirección asociada a un equipo específico (MAC). Para poder hacer esto lo creamos dentro de donde tenemos el ámbito.

![imagen07](./images/instalacion_y_configuracion_dhcp_linux/07.png)

Dentro de este archivo creamos una reserva para nuestro cliente. Para ello ponemos la dirección MAC de mi cliente, una dirección IP que considero conveniente para este equipo y configuramos la puerta de enlace.

![imagen08](./images/instalacion_y_configuracion_dhcp_linux/08.png)

Ahora tenemos que reiniciar el servicio DHCP y ver su estado.

![imagen09](./images/instalacion_y_configuracion_dhcp_linux/09.png)

___

# **6. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello en la consola ponemos el comando ifconfig.

![imagen10](./images/instalacion_y_configuracion_dhcp_linux/10.png)
___

# **6. Otras Opciones.**

Ahora ponemos otras opciones al ámbito. Para poder hacer esto lo creamos dentro de donde tenemos el ámbito.

![imagen11](./images/instalacion_y_configuracion_dhcp_linux/11.png)

Configuramos algunas opciones de servidor además de las habituales, por ejemplo, el tiempo por defecto que tendrán las direcciones IP asignadas a los clientes.

![imagen12](./images/instalacion_y_configuracion_dhcp_linux/12.png)

Ahora tenemos que reiniciar el servicio DHCP y ver su estado.

![imagen13](./images/instalacion_y_configuracion_dhcp_linux/13.png)
___

# **7. Comprobar Funcionamiento DHCP.**

Comprobamos el funcionamiento DHCP configurando adecuadamente la máquina Cliente. Para ello en la consola ponemos el comando ifconfig

![imagen14](./images/instalacion_y_configuracion_dhcp_linux/14.png)

---
