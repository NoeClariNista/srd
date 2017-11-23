___

# **Instalación Y Configuración De Un Servidor Web Avanzado.**

---

## **Carpetas Seguras.**

* Creamos una nueva zona de búsqueda directa en los servicios DNS asociado al dominio miEmpresa. Creamos también una carpeta miEmpresa en C:\ y una subcarpeta ‘principal’.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen02](./images/servidor_web_avanzado/02.png)

![imagen03](./images/servidor_web_avanzado/03.png)

![imagen04](./images/servidor_web_avanzado/04.png)

![imagen05](./images/servidor_web_avanzado/05.png)

![imagen06](./images/servidor_web_avanzado/06.png)

![imagen07](./images/servidor_web_avanzado/07.png)

![imagen08](./images/servidor_web_avanzado/08.png)

![imagen09](./images/servidor_web_avanzado/09.png)

![imagen10](./images/servidor_web_avanzado/10.png)

![imagen11](./images/servidor_web_avanzado/11.png)

* Creamos  un  nuevo  sitio  web  denominado  miEmpresa   en  IIS  asociado  a  la  subcarpeta  anterior  y  con  acceso a través de la dirección www.miEmpresa.com. Actualizamos DNS adecuadamente.

![imagen12](./images/servidor_web_avanzado/12.png)

![imagen13](./images/servidor_web_avanzado/13.png)

![imagen14](./images/servidor_web_avanzado/14.png)

![imagen15](./images/servidor_web_avanzado/15.png)

![imagen16](./images/servidor_web_avanzado/16.png)

![imagen17](./images/servidor_web_avanzado/17.png)

![imagen18](./images/servidor_web_avanzado/18.png)

![imagen19](./images/servidor_web_avanzado/19.png)

* Creamos  un  nuevo  sitio web (denominado ‘pagos’) como subdominio de miEmpresa (pagos.miEmpresa.com) y configuramos este último para ser accedido de forma segura, vía ‘https’.

  * Configuración A: Configuramos el nuevo sitio para que se pueda acceder (sólo) como sitio web seguro (https) con un Certificado Autofirmado.

  ![imagen20](./images/servidor_web_avanzado/20.png)

  ![imagen21](./images/servidor_web_avanzado/21.png)

  ![imagen22](./images/servidor_web_avanzado/22.png)

  ![imagen23](./images/servidor_web_avanzado/23.png)

![imagen24](./images/servidor_web_avanzado/24.png)

![imagen25](./images/servidor_web_avanzado/25.png)

* Creamos el sitio web, asociado a una carpeta (miEmpresa\pagos) y con la configuración adecuada en IIS y en los servicios DNS. Comprobamos el acceso (aún vía ‘http’) con un navegador desde el propio Servidor y desde un Cliente W10.

![imagen26](./images/servidor_web_avanzado/26.png)

![imagen27](./images/servidor_web_avanzado/27.png)

![imagen28](./images/servidor_web_avanzado/28.png)

![imagen29](./images/servidor_web_avanzado/29.png)

![imagen30](./images/servidor_web_avanzado/30.png)

![imagen31](./images/servidor_web_avanzado/31.png)

![imagen32](./images/servidor_web_avanzado/32.png)

![imagen33](./images/servidor_web_avanzado/33.png)

![imagen34](./images/servidor_web_avanzado/34.png)

![imagen35](./images/servidor_web_avanzado/35.png)

  * Configuración B: Crearemos un nuevo sitio seguro (tienda.miempresa.com) con la generación de un Certificado Digital a  través de la aplicación OpenSSL. Para empezar, realizaremos la solicitud de un nuevo certificado de Servidor para nuestro sitio seguro (creamos fichero certreq.txt).

  ![imagen01](./images/servidor_web_avanzado/01.png)

  ![imagen01](./images/servidor_web_avanzado/01.png)

  * Descargamos e instalamos OpenSSL para Windows.

  ![imagen01](./images/servidor_web_avanzado/01.png)

  ![imagen01](./images/servidor_web_avanzado/01.png)

  * A través de OpenSSl generamos un nuevo certificado de servidor (y comprobando los ficheros generados en cada paso): generamos una clave privada de  la  entidad certificadora, creamos un certificado digital de la entidad certificadora y, finalmente, creamos un certificado digital de nuestra web.

  ![imagen01](./images/servidor_web_avanzado/01.png)

  ![imagen01](./images/servidor_web_avanzado/01.png)

  * Importamos el nuevo certificado de servidor creado para completar la petición pendiente en nuestro sitio seguro ‘tienda’.

  ![imagen01](./images/servidor_web_avanzado/01.png)

  ![imagen01](./images/servidor_web_avanzado/01.png)

* Requerimos que nuestros sitio seguros sólo se pueda acceder mediante una conexión segura y reiniciar los sitios web.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Finalmente, accedemos mediante http y mediante https a los sitios seguros desde el propio Servidor y desde un Cliente W10, aceptando los posibles problemas con la entidad certificadora.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

---

## **Carpetas Privadas.**

Vamos a crear un nuevo sitio web (empleados.miEmpresa.com) destinado a almacenar información privada de los empleados, con las siguientes características.

* Necesitamos crear una carpeta empleados (dentro de miEmpresa) y, dentro de esta, cuatro subcarpetas personales con nombres de empleados y una, denominada común, a la que tendrán acceso todos los empleados, pero no otros usuarios sin identificar.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Creamos un nuevo sitio web, como subdominio de nuestro dominio principal, asociado a la carpeta genérica empleados.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Colocamos un fichero index.html diferente en cada una de las carpetas creadas, con el objetivo de poder comprobar el acceso desde un navegador.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Para el sitio web creado y para cada una de sus carpetas, deshabilitamos el acceso anónimo.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Agregamos la función de Autenticación Básica a nuestro Servicio de IIS a través de la Administración del Servidor.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* En Active Directory, crearemos un usuario para cada empleado (tantos   como carpetas personales) y un grupo Empleados que los incluya a todos.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Desactivamos, para la carpeta empleados, los permisos heredables a través de las opciones avanzadas en la ficha de seguridad. Añadimos grupo de Administradores con Control Total y grupo Empleados con Lectura y Ejecución+ Mostrar Carpeta+Leer.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Realizamos el mismo procedimiento para cada una de las carpetas personales de los empleados, colocando como usuarios autorizados el Grupo de Administradores (Control Total) y el empleado propietario de cada carpeta (con los permisos que creas convenientes).

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Realizamos el mismo procedimiento para la carpeta ‘comun’, colocando   como usuarios autorizados el Grupo de Administradores (Control  Total) y el grupo Empleados (con los permisos que creas convenientes).

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

* Comprobamos el acceso, tanto desde el servidor como desde el cliente W10, a las diferentes carpetas con distintos usuarios.

![imagen01](./images/servidor_web_avanzado/01.png)

![imagen01](./images/servidor_web_avanzado/01.png)

---
