___

# **Instalación Y Configuración De Un Servidor Web Avanzado.**

---

## **Carpetas Seguras.**

* Creamos una nueva zona de búsqueda directa en los servicios DNS asociado al dominio miEmpresa.

  ![imagen01](./images/servidor_web_avanzado/01.png)

  Creamos una zona de búsqueda directa.

  ![imagen02](./images/servidor_web_avanzado/02.png)

  Nos sale el asistente para la nueva zona.

  ![imagen03](./images/servidor_web_avanzado/03.png)

  Elegimos el tipo de zona que queremos.

  ![imagen04](./images/servidor_web_avanzado/04.png)

  Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

  ![imagen05](./images/servidor_web_avanzado/05.png)

  Le ponemos un nombre a nuestra zona.

  ![imagen06](./images/servidor_web_avanzado/06.png)

  Permitimos actualizaciones dinámicas seguras.

  ![imagen07](./images/servidor_web_avanzado/07.png)

  Se ha creado la nueva zona.

  ![imagen08](./images/servidor_web_avanzado/08.png)

  Ya contamos con otra zona de búsqueda directa.

  ![imagen09](./images/servidor_web_avanzado/09.png)

* Creamos también una carpeta miEmpresa en C:\ y una subcarpeta ‘principal’.

  ![imagen10](./images/servidor_web_avanzado/10.png)

  ![imagen11](./images/servidor_web_avanzado/11.png)

* Creamos un nuevo sitio web denominado miEmpresa en IIS asociado a la subcarpeta  anterior y con acceso a través de la dirección www.miEmpresa.com.

  ![imagen12](./images/servidor_web_avanzado/12.png)

  ![imagen13](./images/servidor_web_avanzado/13.png)

  ![imagen14](./images/servidor_web_avanzado/14.png)

  ![imagen15](./images/servidor_web_avanzado/15.png)

* Actualizamos el DNS adecuadamente.

  ![imagen16](./images/servidor_web_avanzado/16.png)

  ![imagen17](./images/servidor_web_avanzado/17.png)

  ![imagen18](./images/servidor_web_avanzado/18.png)

* Configuración A: Configuramos el nuevo sitio para que se pueda acceder (sólo) como sitio web seguro (https) con un Certificado Autofirmado.

  ![imagen19](./images/servidor_web_avanzado/19.png)

  ![imagen20](./images/servidor_web_avanzado/20.png)

  ![imagen21](./images/servidor_web_avanzado/21.png)

  ![imagen22](./images/servidor_web_avanzado/22.png)

* Creamos  un  nuevo  sitio web (denominado ‘pagos’) como subdominio de miEmpresa (pagos.miEmpresa.com) y configuramos este último para ser accedido de forma segura, vía ‘https’.

  ![imagen23](./images/servidor_web_avanzado/23.png)

  ![imagen24](./images/servidor_web_avanzado/24.png)

* Creamos el sitio web, asociado a una carpeta (miEmpresa\pagos) y con la configuración adecuada en los servicios DNS.

  ![imagen25](./images/servidor_web_avanzado/25.png)

  ![imagen26](./images/servidor_web_avanzado/26.png)

  ![imagen27](./images/servidor_web_avanzado/27.png)

  ![imagen28](./images/servidor_web_avanzado/28.png)

* Comprobamos el acceso (aún vía ‘http’ y vía ‘https’) con un navegador desde el propio Servidor y desde un Cliente W10.

  * Servidor.

    ![imagen29](./images/servidor_web_avanzado/29.png)

    ![imagen30](./images/servidor_web_avanzado/30.png)

  * Cliente.

    ![imagen31](./images/servidor_web_avanzado/31.png)

    ![imagen32](./images/servidor_web_avanzado/32.png)

* Configuración B: Crearemos un nuevo sitio seguro (tienda.miempresa.com) con la generación de un Certificado Digital a través de la aplicación OpenSSL. Para empezar, realizaremos la solicitud de un nuevo certificado de Servidor para nuestro sitio seguro (creamos fichero certreq.txt).

  ![imagen33](./images/servidor_web_avanzado/33.png)

  ![imagen34](./images/servidor_web_avanzado/34.png)

* Descargamos e instalamos OpenSSL para Windows.

  ![imagen35](./images/servidor_web_avanzado/35.png)

  ![imagen36](./images/servidor_web_avanzado/36.png)

  ![imagen37](./images/servidor_web_avanzado/37.png)

  ![imagen38](./images/servidor_web_avanzado/38.png)

  ![imagen39](./images/servidor_web_avanzado/39.png)

  ![imagen40](./images/servidor_web_avanzado/40.png)

  ![imagen41](./images/servidor_web_avanzado/41.png)

* A través de OpenSSl generamos un nuevo certificado de servidor (y comprobando los ficheros generados en cada paso): generamos una clave privada de  la  entidad certificadora, creamos un certificado digital de la entidad certificadora y, finalmente, creamos un certificado digital de nuestra web.

  ![imagen42](./images/servidor_web_avanzado/42.png)

  ![imagen43](./images/servidor_web_avanzado/43.png)

  ![imagen44](./images/servidor_web_avanzado/44.png)

* Importamos el nuevo certificado de servidor creado para completar la petición pendiente en nuestro sitio seguro ‘tienda’.

  ![imagen45](./images/servidor_web_avanzado/45.png)

  ![imagen46](./images/servidor_web_avanzado/46.png)

  ![imagen47](./images/servidor_web_avanzado/47.png)

  ![imagen48](./images/servidor_web_avanzado/48.png)

  ![imagen49](./images/servidor_web_avanzado/49.png)

  ![imagen50](./images/servidor_web_avanzado/50.png)

* Requerimos que nuestros sitio seguros sólo se pueda acceder mediante una conexión segura y reiniciar los sitios web.

  ![imagen51](./images/servidor_web_avanzado/51.png)

  ![imagen52](./images/servidor_web_avanzado/52.png)

* Finalmente, accedemos mediante http y mediante https a los sitios seguros desde el propio Servidor y desde un Cliente W10, aceptando los posibles problemas con la entidad certificadora.

  * Servidor.

    ![imagen53](./images/servidor_web_avanzado/53.png)

    ![imagen54](./images/servidor_web_avanzado/54.png)

  * Cliente.

    ![imagen55](./images/servidor_web_avanzado/55.png)

    ![imagen56](./images/servidor_web_avanzado/56.png)

---

## **Carpetas Privadas.**

Vamos a crear un nuevo sitio web (empleados.miEmpresa.com) destinado a almacenar información privada de los empleados, con las siguientes características.

* Necesitamos crear una carpeta empleados (dentro de miEmpresa) y, dentro de esta, cuatro subcarpetas personales con nombres de empleados y una, denominada común, a la que tendrán acceso todos los empleados, pero no otros usuarios sin identificar.

  ![imagen57](./images/servidor_web_avanzado/57.png)

  ![imagen58](./images/servidor_web_avanzado/58.png)

* Creamos un nuevo sitio web, como subdominio de nuestro dominio principal, asociado a la carpeta genérica empleados.

  ![imagen59](./images/servidor_web_avanzado/59.png)

  ![imagen60](./images/servidor_web_avanzado/60.png)

  ![imagen61](./images/servidor_web_avanzado/61.png)

  ![imagen62](./images/servidor_web_avanzado/62.png)

* Colocamos un fichero index.html diferente en cada una de las carpetas creadas, con el objetivo de poder comprobar el acceso desde un navegador.

  ![imagen63](./images/servidor_web_avanzado/63.png)

  ![imagen64](./images/servidor_web_avanzado/64.png)

  ![imagen65](./images/servidor_web_avanzado/65.png)

  ![imagen66](./images/servidor_web_avanzado/66.png)

* Para el sitio web creado y para cada una de sus carpetas, deshabilitamos el acceso anónimo.

  ![imagen67](./images/servidor_web_avanzado/67.png)

  ![imagen68](./images/servidor_web_avanzado/68.png)

  ![imagen69](./images/servidor_web_avanzado/69.png)

  ![imagen70](./images/servidor_web_avanzado/70.png)

* Agregamos la función de Autenticación Básica a nuestro Servicio de IIS a través de la Administración del Servidor.

  ![imagen71](./images/servidor_web_avanzado/71.png)

  ![imagen72](./images/servidor_web_avanzado/72.png)

  ![imagen73](./images/servidor_web_avanzado/73.png)

  ![imagen74](./images/servidor_web_avanzado/74.png)

  ![imagen75](./images/servidor_web_avanzado/75.png)

  ![imagen76](./images/servidor_web_avanzado/76.png)

  ![imagen77](./images/servidor_web_avanzado/77.png)

  ![imagen78](./images/servidor_web_avanzado/78.png)

  ![imagen79](./images/servidor_web_avanzado/79.png)

  ![imagen80](./images/servidor_web_avanzado/80.png)

* En Active Directory, crearemos un usuario para cada empleado (tantos   como carpetas personales) y un grupo Empleados que los incluya a todos.

  ![imagen81](./images/servidor_web_avanzado/81.png)

  ![imagen82](./images/servidor_web_avanzado/82.png)

  ![imagen83](./images/servidor_web_avanzado/83.png)

  ![imagen84](./images/servidor_web_avanzado/84.png)

  ![imagen85](./images/servidor_web_avanzado/85.png)

  ![imagen86](./images/servidor_web_avanzado/86.png)

* Desactivamos, para la carpeta empleados, los permisos heredables a través de las opciones avanzadas en la ficha de seguridad. Añadimos grupo de Administradores con Control Total y grupo Empleados con Lectura y Ejecución+ Mostrar Carpeta+Leer.

  ![imagen87](./images/servidor_web_avanzado/87.png)

* Realizamos el mismo procedimiento para cada una de las carpetas personales de los empleados, colocando como usuarios autorizados el Grupo de Administradores (Control Total) y el empleado propietario de cada carpeta.

  ![imagen88](./images/servidor_web_avanzado/88.png)

  ![imagen89](./images/servidor_web_avanzado/89.png)

* Realizamos el mismo procedimiento para la carpeta ‘comun’, colocando   como usuarios autorizados el Grupo de Administradores (Control  Total) y el grupo Empleados.

  ![imagen90](./images/servidor_web_avanzado/90.png)

  ![imagen91](./images/servidor_web_avanzado/91.png)

* Comprobamos el acceso, tanto desde el servidor como desde el cliente W10, a las diferentes carpetas con distintos usuarios.

  ![imagen92](./images/servidor_web_avanzado/92.png)

  * Servidor.

    ![imagen93](./images/servidor_web_avanzado/93.png)

    ![imagen94](./images/servidor_web_avanzado/94.png)

    ![imagen95](./images/servidor_web_avanzado/95.png)

    ![imagen96](./images/servidor_web_avanzado/96.png)

  * Cliente.

    ![imagen97](./images/servidor_web_avanzado/97.png)

    ![imagen98](./images/servidor_web_avanzado/98.png)

    ![imagen99](./images/servidor_web_avanzado/99.png)

    ![imagen100](./images/servidor_web_avanzado/100.png)

---
