___

# **Instalación Y Configuración Del Servicio FTP En Windows 2012 Server.**

---

Desinstalamos el Filezilla en Windows 2012 Server.

Instalamos el Servicio FTP en Windows 2012 Server, a través de Agregar roles y características (IIS).

Accedemos a la creación y configuración de Sitios FTP por medio de la Administración de IIS.

Creamos tres nuevos sitios FTP (en todos ellos se debe poder acceder a través de las IPs del servidor y, en algún caso, de un nombre DNS ftp.tudominio.ext):

  * El primero dominio estará asociado a la unidad C: completa. No debe permitir accesos anónimos. Sin uso de SSL. Sólo el usuario Administrador podrá acceder al sitio. Modos lectura y escritura.  Ahora realiza las siguientes acciones:

    * Examinamos todas las opciones de configuración de la página principal de tu Sitio FTP (IIS) y hacemos una descripción breve de cada una en el informe. No modifiques nada aún.

    aislamiento -> no podrá acceder a carpetas anteriores en el arbol.
    autentificación -> acceso anonimo o básica.
    comprobación ->
    ssl -> los certificados.
    examen de directorios -> como es el estilo de la lista de directorios.
    filtrado de solicitudes -> para no permitir a ciertas máquinas.

    registro -> donde se guard el registro de los errores y accesos.
    reglas de autorizacion -> distintas reglas de permisos a los usuarios y distintos usuarios.
    restricciones direciones ip.
    sesiones actuales -> las sesiones activas ahora mismo.

    * Tratamos de acceder al sitio ftp desde el propio Servidor a través de un navegador y un explorador de archivos.

    * Comprobamos accesos permitidos y denegados. Comprobamos también permisos asignados.

    * Accedemos ahora desde un Cliente Windows de la misma forma. Realizamos comprobaciones.

    * Instalamos el software WinSCP en el cliente Windows, configuramos la conexión a tu sitio ftp y tratamos de establecer conexión y realizamos comprobaciones.

  * El segundo dominio estará asociado al directorio wwwroot de Inetpub. Se permitirá el acceso a todos los usuarios de Active Directory en modo lectura y escritura. No permitimos acceso anónimo y habilitamos en este caso la posibilidad (permitir, no requerir) de conexiones SSL asociadas a uno de los certificados que poseas en IIS. Realizamos diferentes comprobaciones válidas e inválidas de conexión y operaciones, tanto desde el Servidor como desde el Cliente. Realizamos una configuración de conexión SSL desde WinSCP.

  * El tercer dominio estará asociado a una carpeta cualquiera del Servidor que contenga información (archivos y carpetas), pero que no sea importante. Permitiremos acceso anónimo y sólo se podrá consultar y leer. Comprobamos desde Servidor y Cliente.

Debemos crear un nuevo registro DNS que permita acceder a nuestro sitio FTP a través de la dirección ftp.miServer.com (o el dominio que utilices habitualmente).

En un principio es posible que debas detener un sitio web para que pueda iniciarse otro. Tras comprobar el funcionamiento por separado de los sitios, encontrar una solución para que nuestro servidor ofrezca varios sitios FTP simultáneamente.

---
