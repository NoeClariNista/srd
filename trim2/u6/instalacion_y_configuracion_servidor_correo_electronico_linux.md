___

# **Instalación Y Configuración De Un Servidor De Correo En Linux.**

---

Instalamos el Servicio SMTP en Linux, utilizando el Servidor Postfix.

  Descargamos e instalamos postfix con el comando apt-get install postfix.

  ![imagen01](./instalacion_y_configuracion_servidor_correo_electronico_linux/01.png)

  Utilizamos la siguiente configuración de postfix.

    Escogemos la instalación como Sitio de Internet.

    ![imagen02](./instalacion_y_configuracion_servidor_correo_electronico_linux/02.png)

    Creamos el dominio miempresa.com.

    ![imagen03](./instalacion_y_configuracion_servidor_correo_electronico_linux/03.png)

  Comprobamos el Servicio (y puerto) SMTP activo y a la escucha con el comando netstat –utap.

  ![imagen04](./instalacion_y_configuracion_servidor_correo_electronico_linux/04.png)

  Realizamos una prueba de envío de mensaje entre dos usuarios del sistema mediante Telnet.

  ![imagen05](./instalacion_y_configuracion_servidor_correo_electronico_linux/05.png)

  ![imagen06](./instalacion_y_configuracion_servidor_correo_electronico_linux/06.png)

  Instalamos un Cliente de correo electrónico en un Cliente, por  ejemplo, Evolution, para Ubuntu.

  ![imagen07](./instalacion_y_configuracion_servidor_correo_electronico_linux/07.png)

  Creamos dos nuevas entradas en `/etc/hosts`, por ejemplo, smtp.miempresa.com y pop.miempresa.com asociadas a la IP del servidor.

  ![imagen08](./instalacion_y_configuracion_servidor_correo_electronico_linux/08.png)

  ![imagen09](./instalacion_y_configuracion_servidor_correo_electronico_linux/09.png)

  Creamos al menos dos cuentas asociadas a usuarios existentes en el Servidor y asociadas al dominio creado en Postfix. Con figurar datos de las cuentas (dirección correo, servidores entrante y saliente).

  ![imagen10](./instalacion_y_configuracion_servidor_correo_electronico_linux/10.png)

  ![imagen11](./instalacion_y_configuracion_servidor_correo_electronico_linux/11.png)

  ![imagen12](./instalacion_y_configuracion_servidor_correo_electronico_linux/12.png)

  Realizamos el envío de dos correos, uno con cada una de las cuentas creadas. Comprobamos la recepción de estos correos en el Servidor examinando la carpeta `/var/mail`.



Instalamos el Servicio IMAP y Servidor Correo Web SquirrelMail.

  Instalar servicio IMAP con apt-get install dovecot-imapd.

  Comprobar servicio (y puerto) IMAP activo y a la escucha con netstat –utap.

  Instalar aplicación correo web SquirrelMail con apt-get install squirrelmail.

  Carpeta de configuración en `/etc/squirrelmail`.

  Carpeta de aplicación en `/usr/share/squirrelmail`.

  Copiar lineas no comentadas `/etc/squirrelmail/apache.conf` en un nuevo fichero .conf de `/etc/apache2/sites-available`, habilitar sitio y reiniciar apache.

  Acceder vía HTTP en `/localhost/squirrelmail`.

Acceder desde una máquina cliente, vía HTTP, al gestor de correo SquirrelMail instalado

Enviar  y  recibir  correos  entre  las  dos  cuentas  creadas  desde  el  cliente  y  utilizando  el
gestor de correo web SquirrelMail

Comp
robar que los mensajes enviados desde ambas cuentas se siguen encontrando en
los respectivos buzones de los usuarios en /var/mail
o
Instalar servicio POP3:

Instalar servicio POP3 con apt
-
get install
dovecot
-
pop3d

Comprobar servicio (y puerto) POP3 activo y a la escucha con netstat
–
utap

Configurar  MUA  (gestor  de  correo  cliente  Evolution  o  similar)  en  máquina  cliente  para
que  acceda  a  la  recepción  de  correo  a  través  del  protocolo  POP3  instalado  en  el
servidor.

Envia
r  y  recibir  correos  entre  las  dos  cuentas  creadas  desde  el  cliente  y  utilizando  el
gestor de correo del cliente

Comprobar  que  los  correos  enviados  y  recibidos  han  desaparecido  (han  sido  extraídos
por POP3) de los buzones respectivos de los usuarios en /var
/ma
