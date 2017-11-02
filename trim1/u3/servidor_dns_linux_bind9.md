___

>Trabajo Realizado Por:
>
>* Carlos Javier Delgado Hernández.
>
>* Noelia Hernández Domínguez.

---

# **Instalación Y Configuración DNS Linux.**

Realizamos la Instalación y Configuración de un Servidor DNS Bind9 en una máquina Linux.

![imagen01](./images/servidor_dns_linux_bind9/01.png)

`Sudo apt-get install bind9`

![imagen02](./images/servidor_dns_linux_bind9/02.png)

`Configuración de red de la máquina Servidor DNS Ubuntu.`

Se piden las siguientes acciones de Configuración y Prueba del funcionamiento del Servicio.

# **1. Servidor DNS.**

Indicamos a Linux que el Servidor DNS es él mismo, para ello vamos a `/etc/resolv.conf`, lo editamos y ponemos el 127.0.0.1.

![imagen03](./images/servidor_dns_linux_bind9/03.png)

Posteriormente, editamos el archivo localizado en `/etc/resolvconf/resolv.conf.d/base` y asignamos la linea de texto siguiente.

![imagen04](./images/servidor_dns_linux_bind9/04.png)

Con esta configuración conseguimos que el Servidor DNS redireccione hacía si mismo.

---

# **2. Servidor Como Caché DNS.**

Configuramos el Servidor como caché DNS, para ello añadimos en  `/etc/bind/named.conf.options` los reenviadores de DNS con DNS públicos, en nuestro caso añadimos la 8.8.8.8.

![imagen05](./images/servidor_dns_linux_bind9/05.png)

Reiniciamos el Servicio para recargar la nueva configuración establecida.

![imagen06](./images/servidor_dns_linux_bind9/06.png)

`Sudo systemctl restart/status bind9.`

# **3. Comprobaciones.**

Comprobamos la resolución de nombres externos, tanto desde el Servidor como desde un Cliente al que le preste servicio DNS.

![imagen07](./images/servidor_dns_linux_bind9/07.png)

`Ping desde la máquina Servidor.`

![imagen08](./images/servidor_dns_linux_bind9/08.png)

`Configuración de red del Cliente Ubuntu.`

![imagen09](./images/servidor_dns_linux_bind9/09.png)

`Ping desde la máquina Cliente Ubuntu.`

___

# **4. Servidor Como Maestro DNS.**

Configuramos como DNS Maestro instalando un dominio ficticio, por ejemplo una empresa virtual y añadimos una configuración para búsquedas de zona directa y zona inversa en `/etc/bind/named.conf.local`.

![imagen10](./images/servidor_dns_linux_bind9/10.png)

`Establecemos los archivos de configuración "empresa14.db" para la ZBD  y "inverse14.rev" para la ZBI.`

Creamos un archivo de búsqueda directa y otro de búsqueda inversa con los registros que consideramos oportunos. Utilizamos la configuración básica incluida en los archivos db.local (directa) y db.127 (inversa).

![imagen11](./images/servidor_dns_linux_bind9/11.png)

La configuración establecida dentro del archivo "empresa14.db" es.

![imagen12](./images/servidor_dns_linux_bind9/12.png)

La configuración establecida dentro del archivo "inverse14.rev" es.

![imagen13](./images/servidor_dns_linux_bind9/13.png)

Reiniciamos el servicio para establecer la nueva configuración

![imagen14](./images/servidor_dns_linux_bind9/14.png)

---

# **5. Comprobaciones.**

Comprobamos con el comando nslookup/host que se resuelven los nombres desde la consola del Servidor.

![imagen15](./images/servidor_dns_linux_bind9/15.png)

![imagen16](./images/servidor_dns_linux_bind9/16.png)

Comprobamos desde la consola del Cliente que se resuelven correctamente los nombres dados de alta en el Servidor.

![imagen17](./images/servidor_dns_linux_bind9/17.png)

![imagen18](./images/servidor_dns_linux_bind9/18.png)

---

# **6. Servidor Esclavo.**

Clonamos la máquina con el Servidor bind9 instalado y configuramos el nuevo linux para que bind9 se comporte como un Servidor Esclavo.

![imagen19](./images/servidor_dns_linux_bind9/19.png)

Archivo de Configuración "named.conf" del Servidor DNS Ubuntu.

![imagen20](./images/servidor_dns_linux_bind9/20.png)

Archivo de Configuración "named.conf" del Servidor Secundario DNS Ubuntu.

![imagen21](./images/servidor_dns_linux_bind9/21.png)

`Estado del Servicio en el Servidor Secundario.`

![imagen22](./images/servidor_dns_linux_bind9/22.png)

`Estado del Servicio en el Servidor DNS Primario.`

---
