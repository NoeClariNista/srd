___

# **Instalación Y Configuración DHCP Windows.**

___

# **1. Introducción.**

Vamos a crear un manual de instalación y configuración de un servidor DHCP en una máquina con Windows 2012 Server. También utilizaremos una máquina con Windows 10 para hacer que utilice el servidor DHCP.

Durante esta instalación y configuración hay que tener en cuenta que el servidor no debe estar abierto a la red, es decir, hay que configurar el adaptador en red interna para no provocar conflictos de direcciones.

---

# **2. Instalación Del Servicio DHCP En Windows 2012 Server.**

Lo primer que tenemos que hacer es ir a Administrador del Servidor.

![imagen01](./images/01.png)

Luego tenemos que ir a Administrar y vamos a agregar roles y características.

![imagen02](./images/02.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen03](./images/03.png)

![imagen04](./images/04.png)

![imagen05](./images/05.png)

![imagen06](./images/06.png)

![imagen07](./images/07.png)

![imagen08](./images/08.png)

![imagen09](./images/09.png)

![imagen10](./images/10.png)

![imagen11](./images/11.png)

Ahora pinchamos en completar configuración de DHCP.

![imagen12](./images/12.png)

![imagen13](./images/13.png)

![imagen14](./images/14.png)

![imagen15](./images/15.png)

Finalmente terminamos la instalación del Servicio DHCP.

![imagen16](./images/16.png)

# **3. Configuración Del Servicio DHCP Del Primer Ámbito.**

Ahora debo ir a herramientas y luego a DHCP para poder crear un ámbito nuevo asociado a un dominio con un intervalo de direcciones que considero conveniente.

![imagen17](./images/17.png)

![imagen18](./images/18.png)

Ahora dentro de aquí creo el ámbito.

![imagen19](./images/19.png)

![imagen20](./images/20.png)

![imagen21](./images/21.png)

Agrego el nombre que le quiero dar al ámbito y también una pequeña descripción.

![imagen22](./images/22.png)

Añado una dirección IP con máscara de clase B.

![imagen23](./images/23.png)

No agrego ninguna exclusión, ya que en el intervalo de direcciones IP no añadí las que necesito para otras cosas del ámbito.

![imagen24](./images/24.png)

![imagen25](./images/25.png)

![imagen26](./images/26.png)

Configuramos la puerta de enlace con una de las direcciones que deje fuera del intervalo de direcciones IP.

![imagen27](./images/27.png)

También configuro los servidores DNS.

![imagen28](./images/28.png)

![imagen29](./images/29.png)

![imagen30](./images/30.png)

![imagen31](./images/31.png)

Finalmente hemos creado nuestro ámbito con las configuraciones que hemos considerado convenientes.

![imagen32](./images/32.png)

# **4. Comprobar Funcionamiento DHCP Del Primer Ámbito.**

Para comprobar que funciona el DHCP tenemos que ir a nuestra máquina virtual de Windows 10 y poner su dirección IP automática, esto lo hago para que coja señal de mi servidor DHCP.

![imagen33](./images/33.png)

![imagen34](./images/34.png)

# **5. Configuración Del Servicio DHCP Del Segundo Ámbito.**

Denuevo creamos otro nuevo ámbito con otros parámetros que considere oprtunos y que puedan estar ambos ámbitos a la vez.

Ahora dentro de aquí creo el nuevo ámbito.

![imagen35](./images/35.png)

![imagen36](./images/36.png)

![imagen37](./images/37.png)

Agrego el nombre que le quiero dar al ámbito y también una pequeña descripción.

![imagen38](./images/38.png)

Añado una dirección IP con máscara de clase C.

![imagen39](./images/39.png)

No agrego ninguna exclusión, ya que en el intervalo de direcciones IP no añadí las que necesito para otras cosas del ámbito.

![imagen40](./images/40.png)

![imagen41](./images/41.png)

![imagen42](./images/42.png)

Configuramos la puerta de enlace con una de las direcciones que deje fuera del intervalo de direcciones IP.

![imagen43](./images/43.png)

También configuro los servidores DNS.

![imagen44](./images/44.png)

![imagen45](./images/45.png)

![imagen46](./images/46.png)

![imagen47](./images/47.png)

Finalmente hemos creado nuestro ámbito con las configuraciones que hemos considerado oportunas.

![imagen48](./images/48.png)

# **6. Comprobar Funcionamiento DHCP Del Segundo Ámbito.**

Ahora tenemos que inactivar el ámbito dominio y poner activo el segundo ámbito.

![imagen49](./images/49.png)

Para comprobar que funciona el DHCP tenemos que ir a nuestra máquina virtual de Windows 10, poner su dirección IP automática, esto lo hago para que coja señal de mi servidor DHCP.

![imagen50](./images/50.png)

![imagen51](./images/51.png)

# **7. Superámbito DHCP.**

Ahora creo un superámbito DHCP que incluya a los dos ámbitos anteriores.

![imagen52](./images/52.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen53](./images/53.png)

![imagen54](./images/54.png)

![imagen55](./images/55.png)

![imagen56](./images/56.png)

![imagen57](./images/57.png)

![imagen58](./images/58.png)

![imagen59](./images/59.png)

Finalmente el superámbito esta creado.

![imagen60](./images/60.png)

Tenemos que borrar una dirección IP de cliente que se guarda durante el tiempo que le marque en la configuración.

![imagen61](./images/61.png)

![imagen62](./images/62.png)

Vamos desactivando cada ámbito y así vemos que se conecta al otro ámbito.

![imagen63](./images/63.png)

![imagen64](./images/64.png)

![imagen65](./images/65.png)

![imagen66](./images/66.png)

![imagen67](./images/67.png)
