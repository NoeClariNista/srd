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

  ![imagen01](./instalacion_y_configuracion_servidor_correo_electronico_linux/01.png)

  Utilizamos la siguiente configuración de Postfix.

    Escogemos la instalación como Sitio de Internet.

    ![imagen02](./instalacion_y_configuracion_servidor_correo_electronico_linux/02.png)

    Creamos el dominio `miempresa.com`.

    ![imagen03](./instalacion_y_configuracion_servidor_correo_electronico_linux/03.png)

  Comprobamos el Servicio (y puerto) SMTP activo y a la escucha con el comando netstat –utap.

  ![imagen04](./instalacion_y_configuracion_servidor_correo_electronico_linux/04.png)

  Realizamos una prueba de envío de mensaje entre dos usuarios del sistema mediante Telnet.

  ![imagen05](./instalacion_y_configuracion_servidor_correo_electronico_linux/05.png)

  ![imagen06](./instalacion_y_configuracion_servidor_correo_electronico_linux/06.png)

  Instalamos un Cliente de correo electrónico en un Cliente, por ejemplo, Evolution, para Ubuntu.

  ![imagen07](./instalacion_y_configuracion_servidor_correo_electronico_linux/07.png)

  Creamos dos nuevas entradas en `/etc/hosts`, por ejemplo, `smtp.miempresa.com` y `pop.miempresa.com` asociadas a la IP del Servidor, es decir, asociada a 172.18.20.41.

  ![imagen08](./instalacion_y_configuracion_servidor_correo_electronico_linux/08.png)

  ![imagen09](./instalacion_y_configuracion_servidor_correo_electronico_linux/09.png)

  Creamos al menos dos cuentas asociadas a usuarios existentes en el Servidor y asociadas al dominio creado en Postfix. Con figurar datos de las cuentas (dirección correo, servidores entrante y saliente).

  ![imagen10](./instalacion_y_configuracion_servidor_correo_electronico_linux/10.png)

  ![imagen11](./instalacion_y_configuracion_servidor_correo_electronico_linux/11.png)

  ![imagen12](./instalacion_y_configuracion_servidor_correo_electronico_linux/12.png)

  ![imagen13](./instalacion_y_configuracion_servidor_correo_electronico_linux/13.png)

  ![imagen14](./instalacion_y_configuracion_servidor_correo_electronico_linux/14.png)

  ![imagen15](./instalacion_y_configuracion_servidor_correo_electronico_linux/15.png)

  ![imagen16](./instalacion_y_configuracion_servidor_correo_electronico_linux/16.png)

  ![imagen17](./instalacion_y_configuracion_servidor_correo_electronico_linux/17.png)

  ![imagen18](./instalacion_y_configuracion_servidor_correo_electronico_linux/18.png)

  ![imagen19](./instalacion_y_configuracion_servidor_correo_electronico_linux/19.png)

  ![imagen20](./instalacion_y_configuracion_servidor_correo_electronico_linux/20.png)

  ![imagen21](./instalacion_y_configuracion_servidor_correo_electronico_linux/21.png)

  ![imagen22](./instalacion_y_configuracion_servidor_correo_electronico_linux/22.png)

  ![imagen23](./instalacion_y_configuracion_servidor_correo_electronico_linux/23.png)

  ![imagen24](./instalacion_y_configuracion_servidor_correo_electronico_linux/24.png)

  ![imagen25](./instalacion_y_configuracion_servidor_correo_electronico_linux/25.png)

  ![imagen26](./instalacion_y_configuracion_servidor_correo_electronico_linux/26.png)

  ![imagen27](./instalacion_y_configuracion_servidor_correo_electronico_linux/27.png)

  ![imagen28](./instalacion_y_configuracion_servidor_correo_electronico_linux/28.png)

  ![imagen29](./instalacion_y_configuracion_servidor_correo_electronico_linux/29.png)

  ![imagen30](./instalacion_y_configuracion_servidor_correo_electronico_linux/30.png)

  Realizamos el envío de dos correos, uno con cada una de las cuentas creadas. Comprobamos la recepción de estos correos en el Servidor examinando la carpeta `/var/mail`.

  ![imagen31](./instalacion_y_configuracion_servidor_correo_electronico_linux/31.png)

  ![imagen32](./instalacion_y_configuracion_servidor_correo_electronico_linux/32.png)

  ![imagen33](./instalacion_y_configuracion_servidor_correo_electronico_linux/33.png)

  ![imagen34](./instalacion_y_configuracion_servidor_correo_electronico_linux/34.png)

  ![imagen35](./instalacion_y_configuracion_servidor_correo_electronico_linux/35.png)

  ![imagen36](./instalacion_y_configuracion_servidor_correo_electronico_linux/36.png)

Instalamos el Servicio IMAP y Servidor Correo Web SquirrelMail.

  Instalar servicio IMAP con apt-get install dovecot-imapd.

  ![imagen37](./instalacion_y_configuracion_servidor_correo_electronico_linux/37.png)

  Comprobar servicio (y puerto) IMAP activo y a la escucha con netstat –utap.

  ![imagen38](./instalacion_y_configuracion_servidor_correo_electronico_linux/38.png)

  Instalar aplicación correo web SquirrelMail con apt-get install squirrelmail.

  ![imagen39](./instalacion_y_configuracion_servidor_correo_electronico_linux/39.png)

  Carpeta de configuración en `/etc/squirrelmail`.

  ![imagen40](./instalacion_y_configuracion_servidor_correo_electronico_linux/40.png)

  Carpeta de aplicación en `/usr/share/squirrelmail`.

  ![imagen41](./instalacion_y_configuracion_servidor_correo_electronico_linux/41.png)

  Copiar líneas no comentadas `/etc/squirrelmail/apache.conf` en un nuevo fichero .conf de `/etc/apache2/sites-available`, habilitar sitio y reiniciar apache.

  ![imagen42](./instalacion_y_configuracion_servidor_correo_electronico_linux/42.png)

  ![imagen43](./instalacion_y_configuracion_servidor_correo_electronico_linux/43.png)

  ![imagen44](./instalacion_y_configuracion_servidor_correo_electronico_linux/44.png)

  ![imagen45](./instalacion_y_configuracion_servidor_correo_electronico_linux/45.png)

  ![imagen46](./instalacion_y_configuracion_servidor_correo_electronico_linux/46.png)

  Acceder vía HTTP en `/localhost/squirrelmail`.

  ![imagen47](./instalacion_y_configuracion_servidor_correo_electronico_linux/47.png)

  ![imagen48](./instalacion_y_configuracion_servidor_correo_electronico_linux/48.png)

  ![imagen49](./instalacion_y_configuracion_servidor_correo_electronico_linux/49.png)

  ![imagen50](./instalacion_y_configuracion_servidor_correo_electronico_linux/50.png)

  Acceder desde una máquina cliente, vía HTTP, al gestor de correo SquirrelMail instalado.

  ![imagen51](./instalacion_y_configuracion_servidor_correo_electronico_linux/51.png)

  ![imagen52](./instalacion_y_configuracion_servidor_correo_electronico_linux/52.png)

  ![imagen53](./instalacion_y_configuracion_servidor_correo_electronico_linux/53.png)

  Enviar  y  recibir  correos  entre  las  dos  cuentas  creadas  desde  el  Cliente  y  utilizando  el gestor de correo web SquirrelMail.

  ![imagen54](./instalacion_y_configuracion_servidor_correo_electronico_linux/54.png)

  ![imagen55](./instalacion_y_configuracion_servidor_correo_electronico_linux/55.png)

  ![imagen56](./instalacion_y_configuracion_servidor_correo_electronico_linux/56.png)

  ![imagen57](./instalacion_y_configuracion_servidor_correo_electronico_linux/57.png)

  ![imagen58](./instalacion_y_configuracion_servidor_correo_electronico_linux/58.png)

  ![imagen59](./instalacion_y_configuracion_servidor_correo_electronico_linux/59.png)

  ![imagen60](./instalacion_y_configuracion_servidor_correo_electronico_linux/60.png)

  ![imagen61](./instalacion_y_configuracion_servidor_correo_electronico_linux/61.png)

  ![imagen62](./instalacion_y_configuracion_servidor_correo_electronico_linux/62.png)

  ![imagen63](./instalacion_y_configuracion_servidor_correo_electronico_linux/63.png)

  ![imagen64](./instalacion_y_configuracion_servidor_correo_electronico_linux/64.png)

  Comprobar que los mensajes enviados desde ambas cuentas se siguen encontrando en los respectivos buzones de los usuarios en `/var/mail`.

  ![imagen65](./instalacion_y_configuracion_servidor_correo_electronico_linux/65.png)

  ![imagen66](./instalacion_y_configuracion_servidor_correo_electronico_linux/66.png)

Instalar Servicio POP3.

  Instalar servicio POP3 con el comando apt-get install dovecot-pop3d.

  ![imagen67](./instalacion_y_configuracion_servidor_correo_electronico_linux/67.png)

  Comprobar servicio (y puerto) POP3 activo y a la escucha con netstat –utap.

  ![imagen68](./instalacion_y_configuracion_servidor_correo_electronico_linux/68.png)

  Configurar  MUA  (gestor  de  correo  cliente  Evolution  o  similar)  en  máquina  Cliente  para que  acceda  a  la  recepción  de  correo  a  través  del  protocolo  POP3  instalado  en  el Servidor.



  Enviar  y  recibir  correos  entre  las  dos  cuentas  creadas  desde  el  cliente  y  utilizando  el gestor de correo del cliente.



  Comprobar  que  los  correos  enviados  y  recibidos  han  desaparecido  (han  sido  extraídos por POP3) de los buzones respectivos de los usuarios en `/var/mail`.



---
