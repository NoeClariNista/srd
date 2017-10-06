___

# **Instalación Y Configuración DHCP Windows.**
___

# **1. Introducción.**

Vamos a crear un manual de instalación y configuración de un servidor DHCP en una máquina con Windows 2012 Server. También utilizaremos una máquina con Windows 10 para hacer que utilice el servidor DHCP.

Durante esta instalación y configuración hay que tener en cuenta que el servidor no debe estar abierto a la red, es decir, hay que configurar el adaptador en red interna para no provocar conflictos de direcciones.

---

# **2. Instalación Del Servicio DHCP En Windows 2012 Server.**

Lo primer que tenemos que hacer es ir a Administrador del Servidor.

![imagen01](./images/instalacion_y_configuracion_dhcp_windows/01.png)

Luego tenemos que ir a Administrar y vamos a agregar roles y características.

![imagen02](./images/instalacion_y_configuracion_dhcp_windows/02.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen03](./images/instalacion_y_configuracion_dhcp_windows/03.png)

![imagen04](./images/instalacion_y_configuracion_dhcp_windows/04.png)

![imagen05](./images/instalacion_y_configuracion_dhcp_windows/05.png)

![imagen06](./images/instalacion_y_configuracion_dhcp_windows/06.png)

![imagen07](./images/instalacion_y_configuracion_dhcp_windows/07.png)

![imagen08](./images/instalacion_y_configuracion_dhcp_windows/08.png)

![imagen09](./images/instalacion_y_configuracion_dhcp_windows/09.png)

![imagen10](./images/instalacion_y_configuracion_dhcp_windows/10.png)

![imagen11](./images/instalacion_y_configuracion_dhcp_windows/11.png)

Ahora pinchamos en completar configuración de DHCP.

![imagen12](./images/instalacion_y_configuracion_dhcp_windows/12.png)

![imagen13](./images/instalacion_y_configuracion_dhcp_windows/13.png)

![imagen14](./images/instalacion_y_configuracion_dhcp_windows/14.png)

![imagen15](./images/instalacion_y_configuracion_dhcp_windows/15.png)

Finalmente terminamos la instalación del Servicio DHCP.

![imagen16](./images/instalacion_y_configuracion_dhcp_windows/16.png)

# **3. Configuración Del Servicio DHCP Del Primer Ámbito.**

Ahora debo ir a herramientas y luego a DHCP para poder crear un ámbito nuevo asociado a un dominio con un intervalo de direcciones que considero conveniente.

![imagen17](./images/instalacion_y_configuracion_dhcp_windows/17.png)

![imagen18](./images/instalacion_y_configuracion_dhcp_windows/18.png)

Ahora dentro de aquí creo el ámbito.

![imagen19](./images/instalacion_y_configuracion_dhcp_windows/19.png)

![imagen20](./images/instalacion_y_configuracion_dhcp_windows/20.png)

![imagen21](./images/instalacion_y_configuracion_dhcp_windows/21.png)

Agrego el nombre que le quiero dar al ámbito y también una pequeña descripción.

![imagen22](./images/instalacion_y_configuracion_dhcp_windows/22.png)

Añado una dirección IP con máscara de clase B.

![imagen23](./images/instalacion_y_configuracion_dhcp_windows/23.png)

No agrego ninguna exclusión, ya que en el intervalo de direcciones IP no añadí las que necesito para otras cosas del ámbito.

![imagen24](./images/instalacion_y_configuracion_dhcp_windows/24.png)

![imagen25](./images/instalacion_y_configuracion_dhcp_windows/25.png)

![imagen26](./images/instalacion_y_configuracion_dhcp_windows/26.png)

Configuramos la puerta de enlace con una de las direcciones que deje fuera del intervalo de direcciones IP.

![imagen27](./images/instalacion_y_configuracion_dhcp_windows/27.png)

También configuro los servidores DNS.

![imagen28](./images/instalacion_y_configuracion_dhcp_windows/28.png)

![imagen29](./images/instalacion_y_configuracion_dhcp_windows/29.png)

![imagen30](./images/instalacion_y_configuracion_dhcp_windows/30.png)

![imagen31](./images/instalacion_y_configuracion_dhcp_windows/31.png)

Finalmente hemos creado nuestro ámbito con las configuraciones que hemos considerado convenientes.

![imagen32](./images/instalacion_y_configuracion_dhcp_windows/32.png)

# **4. Comprobar Funcionamiento DHCP Del Primer Ámbito.**

Para comprobar que funciona el DHCP tenemos que ir a nuestra máquina virtual de Windows 10 y poner su dirección IP automática, esto lo hago para que coja señal de mi servidor DHCP.

![imagen33](./images/instalacion_y_configuracion_dhcp_windows/33.png)

![imagen34](./images/instalacion_y_configuracion_dhcp_windows/34.png)

# **5. Configuración Del Servicio DHCP Del Segundo Ámbito.**

Denuevo creamos otro nuevo ámbito con otros parámetros que considere oprtunos y que puedan estar ambos ámbitos a la vez.

Ahora dentro de aquí creo el nuevo ámbito.

![imagen35](./images/instalacion_y_configuracion_dhcp_windows/35.png)

![imagen36](./images/instalacion_y_configuracion_dhcp_windows/36.png)

![imagen37](./images/instalacion_y_configuracion_dhcp_windows/37.png)

Agrego el nombre que le quiero dar al ámbito y también una pequeña descripción.

![imagen38](./images/instalacion_y_configuracion_dhcp_windows/38.png)

Añado una dirección IP con máscara de clase C.

![imagen39](./images/instalacion_y_configuracion_dhcp_windows/39.png)

No agrego ninguna exclusión, ya que en el intervalo de direcciones IP no añadí las que necesito para otras cosas del ámbito.

![imagen40](./images/instalacion_y_configuracion_dhcp_windows/40.png)

![imagen41](./images/instalacion_y_configuracion_dhcp_windows/41.png)

![imagen42](./images/instalacion_y_configuracion_dhcp_windows/42.png)

Configuramos la puerta de enlace con una de las direcciones que deje fuera del intervalo de direcciones IP.

![imagen43](./images/instalacion_y_configuracion_dhcp_windows/43.png)

También configuro los servidores DNS.

![imagen44](./images/instalacion_y_configuracion_dhcp_windows/44.png)

![imagen45](./images/instalacion_y_configuracion_dhcp_windows/45.png)

![imagen46](./images/instalacion_y_configuracion_dhcp_windows/46.png)

![imagen47](./images/instalacion_y_configuracion_dhcp_windows/47.png)

Finalmente hemos creado nuestro ámbito con las configuraciones que hemos considerado oportunas.

![imagen48](./images/instalacion_y_configuracion_dhcp_windows/48.png)

# **6. Comprobar Funcionamiento DHCP Del Segundo Ámbito.**

Ahora tenemos que inactivar el ámbito dominio y poner activo el segundo ámbito.

![imagen49](./images/instalacion_y_configuracion_dhcp_windows/49.png)

Para comprobar que funciona el DHCP tenemos que ir a nuestra máquina virtual de Windows 10, poner su dirección IP automática, esto lo hago para que coja señal de mi servidor DHCP.

![imagen50](./images/instalacion_y_configuracion_dhcp_windows/50.png)

![imagen51](./images/instalacion_y_configuracion_dhcp_windows/51.png)

# **7. Superámbito DHCP.**

Ahora creo un superámbito DHCP que incluya a los dos ámbitos anteriores.

![imagen52](./images/instalacion_y_configuracion_dhcp_windows/52.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen53](./images/instalacion_y_configuracion_dhcp_windows/53.png)

![imagen54](./images/instalacion_y_configuracion_dhcp_windows/54.png)

![imagen55](./images/instalacion_y_configuracion_dhcp_windows/55.png)

![imagen56](./images/instalacion_y_configuracion_dhcp_windows/56.png)

![imagen57](./images/instalacion_y_configuracion_dhcp_windows/57.png)

![imagen58](./images/instalacion_y_configuracion_dhcp_windows/58.png)

![imagen59](./images/instalacion_y_configuracion_dhcp_windows/59.png)

Finalmente el superámbito esta creado.

![imagen60](./images/instalacion_y_configuracion_dhcp_windows/60.png)

Tenemos que borrar una dirección IP de cliente que se guarda durante el tiempo que le marque en la configuración.

![imagen61](./images/instalacion_y_configuracion_dhcp_windows/61.png)

![imagen62](./images/instalacion_y_configuracion_dhcp_windows/62.png)

Vamos desactivando cada ámbito y así vemos que se conecta al otro ámbito.

![imagen63](./images/instalacion_y_configuracion_dhcp_windows/63.png)

![imagen64](./images/instalacion_y_configuracion_dhcp_windows/64.png)

![imagen65](./images/instalacion_y_configuracion_dhcp_windows/65.png)

![imagen66](./images/instalacion_y_configuracion_dhcp_windows/66.png)

![imagen67](./images/instalacion_y_configuracion_dhcp_windows/67.png)
