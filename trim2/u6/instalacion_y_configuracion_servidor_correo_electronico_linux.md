Práctica de
Linux
-
SRD
–
2º ASIR
Instalación y Configuración de un Servidor
de Correo

Siguiendo los pasos detallados
en las guías y tutoriales
proporcionados:
o
Instalar
s
ervicio
SMTP
en
Linux, utilizando el servidor Postfix:

Descargar e instalar postfix
: apt
-
get install postfix
.

Configuración de postfix:
o
Escoger instalación como Sitio de Internet
o
Crear dominio miempresa.com o similar

Comprobar servicio (y puerto) SMTP activo y a la escucha con netstat
–
utap

Realizar  una  prueba  de  envío  de  mensaje  entre  dos  usuarios  del  sistema  mediante
telnet,  tal  y  como  se  indica  en  el  ejemplo  del  apartado
Prueba  de  Funcionamiento
del
documento pdf.

Instalar  un  cliente  de  correo  electrónico  en  un  cliente  (por  ejemplo
Evolution,  para
Ubuntu).

Crear  dos  nuevas  entradas  en  /etc/hosts:  smtp.miempresa.com  y  pop.miempresa.com
asociadas a la IP del servidor.

Crear al menos dos cuentas asociadas a usuarios existentes en el servidor y asociadas al
dominio creado en Postfix. Con
figurar datos de las cuentas (dirección correo, servidores
entrante y saliente).

Realizar  envío  de  dos  correos,  uno  con  cada  una  de  las  cuentas  creadas.  Comprobar  la
recepción de estos correos en el servidor examinando la carpeta /var/mail.
o
Instalar servic
io IMAP y servidor Correo Web SquirrelMail:

Instalar servicio IMAP con apt
-
get install
dovecot
-
imapd

Comprobar servicio (y puerto) IMAP activo y a la escucha con netstat
–
utap

Instalar aplicación correo web SquirrelMail
con apt
-
get install squirrelmail

Carpeta
de c
onfiguración en /etc/squirrelmail

Carpeta de a
plicación en /usr/share/squirrelmail

Copiar lineas
no comentadas
/etc/squirrelmail/apache.conf
en
un nuevo fichero .conf de
/etc/apache2/sites
-
available
, habilitar sitio
y reiniciar apache

Acceder vía HTTP en /localhost/squirrelmail

Enlaces
para consulta y resolución de posibles problemas:
o
http://pedroreina.net/recetas/squirrelmail.html
o
http://eric
-
blue.com/2006/06/18/enabling
-
plain
-
text
-
login
-
for
-
uw
-
imap/
o
http://www.saslibre.com/howto
-
/87
-
uw.html
o
http://www.directadmi
n.com/forum/showthread.php?t=19371&page=1

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
