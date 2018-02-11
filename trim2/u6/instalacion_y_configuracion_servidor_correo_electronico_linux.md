___

>Trabajo Realizado Por:
>
>* Noelia Hernández Domínguez.
>
>* Omar Hernández Padrón.

---

# **Instalación Y Configuración De Un Servidor De Correo En Linux.**

---

Instalamos el Servicio SMTP en Linux, utilizando el Servidor Postfix.

  Descargamos e instalamos Postfix con el comando apt-get install postfix.

  ![imagen01](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/01.png)

  Utilizamos la siguiente configuración de Postfix.

  Escogemos la instalación como Sitio de Internet.

  ![imagen02](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/02.png)

  Creamos el dominio `miempresa.com`.

  ![imagen03](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/03.png)

  Comprobamos el Servicio (y puerto) SMTP activo y a la escucha con el comando netstat –utap.

  ![imagen04](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/04.png)

  Realizamos una prueba de envío de mensaje entre dos usuarios del sistema mediante Telnet.

  ![imagen05](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/05.png)

  ![imagen06](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/06.png)

  Instalamos un Cliente de correo electrónico en un Cliente, por ejemplo, Evolution, para Ubuntu.

  ![imagen07](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/07.png)

  Creamos dos nuevas entradas en `/etc/hosts`, por ejemplo, `smtp.miempresa.com` y `pop.miempresa.com` asociadas a la IP del Servidor, es decir, asociada a 172.18.20.41.

  ![imagen08](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/08.png)

  ![imagen09](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/09.png)

  Creamos dos cuentas asociadas a usuarios existentes en el Servidor y asociadas al dominio creado en Postfix.

  * Cuentas en el Servidor.

  ![imagen10](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/10.png)

  * Cuentas en el Cliente.

  ![imagen11](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/11.png)

  Configuramos los datos de las cuentas (dirección correo, servidores entrante y saliente).

  ![imagen12](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/12.png)

  ![imagen13](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/13.png)

  ![imagen14](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/14.png)

  ![imagen15](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/15.png)

  ![imagen16](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/16.png)

  ![imagen17](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/17.png)

  ![imagen18](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/18.png)

  ![imagen19](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/19.png)

  ![imagen20](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/20.png)

  ![imagen21](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/21.png)

  ![imagen22](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/22.png)

  ![imagen23](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/23.png)

  ![imagen24](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/24.png)

  ![imagen25](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/25.png)

  ![imagen26](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/26.png)

  ![imagen27](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/27.png)

  ![imagen28](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/28.png)

  ![imagen29](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/29.png)

  ![imagen30](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/30.png)

  Realizamos el envío de dos correos, uno con cada una de las cuentas creadas.

  ![imagen31](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/31.png)

  ![imagen32](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/32.png)

  ![imagen33](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/33.png)

  ![imagen34](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/34.png)

  Comprobamos la recepción de estos correos en el Servidor examinando la carpeta `/var/mail`.

  ![imagen35](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/35.png)

  ![imagen36](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/36.png)

Instalamos el Servicio IMAP y Servidor Correo Web SquirrelMail.

  Instalamos el Servicio IMAP con el comando apt-get install dovecot-imapd.

  ![imagen37](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/37.png)

  Comprobamos el Servicio (y puerto) IMAP activo y a la escucha con el comando netstat –utap.

  ![imagen38](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/38.png)

  Instalamos la aplicación correo web SquirrelMail con el comando apt-get install squirrelmail.

  ![imagen39](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/39.png)

  La carpeta de configuración la podemos ver en `/etc/squirrelmail`.

  ![imagen40](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/40.png)

  La carpeta de aplicación la podemos ver en `/usr/share/squirrelmail`.

  ![imagen41](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/41.png)

  Copiamos las líneas no comentadas del fichero `/etc/squirrelmail/apache.conf` en un nuevo fichero .conf de `/etc/apache2/sites-available`.

  ![imagen42](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/42.png)

  ![imagen43](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/43.png)

  ![imagen44](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/44.png)

  Habilitamos el sitio.

  ![imagen45](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/45.png)

  Reiniciamos Apache.

  ![imagen46](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/46.png)

  Accedemos vía HTTP en `/localhost/squirrelmail`.

  ![imagen47](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/47.png)

  ![imagen48](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/48.png)

  ![imagen49](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/49.png)

  ![imagen50](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/50.png)

  Accedemos desde una máquina Cliente, vía HTTP, al gestor de correo SquirrelMail instalado.

  ![imagen51](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/51.png)

  ![imagen52](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/52.png)

  ![imagen53](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/53.png)

  Enviamos y recibimos correos entre las dos cuentas creadas desde el Cliente utilizando el gestor de correo web SquirrelMail.

  ![imagen54](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/54.png)

  ![imagen55](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/55.png)

  ![imagen56](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/56.png)

  ![imagen57](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/57.png)

  ![imagen58](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/58.png)

  ![imagen59](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/59.png)

  ![imagen60](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/60.png)

  ![imagen61](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/61.png)

  ![imagen62](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/62.png)

  ![imagen63](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/63.png)

  ![imagen64](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/64.png)

  Comprobamos que los mensajes enviados desde ambas cuentas se siguen encontrando en los respectivos buzones de los usuarios en `/var/mail`.

  ![imagen65](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/65.png)

  ![imagen66](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/66.png)

Instalamos el Servicio POP3.

  Instalamos el Servicio POP3 con el comando apt-get install dovecot-pop3d.

  ![imagen67](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/67.png)

  Comprobamos el Servicio (y puerto) POP3 activo y a la escucha con el comando netstat –utap.

  ![imagen68](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/68.png)

  Configuramos MUA (gestor de correo cliente Evolution) en la máquina Cliente para que acceda a la recepción de correo a través del protocolo POP3 instalado en el Servidor.

  Borramos los usuarios creados.

  ![imagen69](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/69.png)

  Creamos denuevo los usuarios pero esta vez con el Servicio POP3.

  ![imagen70](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/70.png)

  ![imagen71](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/71.png)

  ![imagen72](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/72.png)

  ![imagen73](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/73.png)

  ![imagen74](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/74.png)

  ![imagen75](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/75.png)

  ![imagen76](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/76.png)

  ![imagen77](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/77.png)

  ![imagen78](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/78.png)

  ![imagen79](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/79.png)

  ![imagen80](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/80.png)

  ![imagen81](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/81.png)

  ![imagen82](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/82.png)

  ![imagen83](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/83.png)

  ![imagen84](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/84.png)

  ![imagen85](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/85.png)

  ![imagen86](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/86.png)

  Vamos al Servidor. Vamos a la configuración de Dovecot y descomentamos una línea en el fichero `10-auth.conf`.

  ![imagen87](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/87.png)

  ![imagen88](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/88.png)

  Reiniciamos el Servicio de Dovecot.

  ![imagen89](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/89.png)

  Enviamos y recibimos correos entre las dos cuentas creadas desde el Cliente y utilizando el gestor de correo del Cliente.

  ![imagen90](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/90.png)

  ![imagen91](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/91.png)

  ![imagen92](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/92.png)

  ![imagen93](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/93.png)

  Comprobamos que los correos enviados y recibidos no han desaparecido de los buzones respectivos de los usuarios en `/var/mail`.

  ![imagen94](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/94.png)

  ![imagen95](./images/instalacion_y_configuracion_servidor_correo_electronico_linux/95.png)


---
