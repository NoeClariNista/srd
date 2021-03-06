___

# **Servidor Web Básico.**

___

## **1. Instalación, Configuración Y Creación De Sitios Web.**

Instalamos IIS en Windows 2012 Server.

Lo primero que tenemos que hacer es ir a Administrador del Servidor.

![imagen01](./images/servidor_web_basico/01.png)

Luego tenemos que ir a Administrar y vamos a Agregar roles y características.

![imagen02](./images/servidor_web_basico/02.png)

El resto de pasos los realizamos como se pueden ver en las imágenes.

![imagen03](./images/servidor_web_basico/03.png)

![imagen04](./images/servidor_web_basico/04.png)

![imagen05](./images/servidor_web_basico/05.png)

![imagen06](./images/servidor_web_basico/06.png)

![imagen07](./images/servidor_web_basico/07.png)

![imagen08](./images/servidor_web_basico/08.png)

![imagen09](./images/servidor_web_basico/09.png)

![imagen10](./images/servidor_web_basico/10.png)

![imagen11](./images/servidor_web_basico/11.png)

![imagen12](./images/servidor_web_basico/12.png)

Finalmente terminamos la instalación de IIS en Windows 2012 Server.

![imagen13](./images/servidor_web_basico/13.png)

Ahora comprobamos el acceso a nuestro Servidor Web (localhost) desde un navegador web (debe aparecer una página en construcción).

![imagen14](./images/servidor_web_basico/14.png)

Entramos en el Cliente Windows 10 y accedemos, desde un navegador web, a la página principal del Servidor a través de la IP del Servidor, 172.18.20.11.

![imagen15](./images/servidor_web_basico/15.png)

Ahora tenemos que crear en la configuración DNS una nueva zona de búsqueda directa en el Servidor.

Creamos una zona de búsqueda directa.

![imagen16](./images/servidor_web_basico/16.png)

Nos sale el asistente para la nueva zona.

![imagen17](./images/servidor_web_basico/17.png)

Elegimos el tipo de zona que queremos.

![imagen18](./images/servidor_web_basico/18.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen19](./images/servidor_web_basico/19.png)

Le ponemos un nombre a nuestra zona.

![imagen20](./images/servidor_web_basico/20.png)

Permitimos actualizaciones dinámicas seguras.

![imagen21](./images/servidor_web_basico/21.png)

Se ha creado la nueva zona.

![imagen22](./images/servidor_web_basico/22.png)

Ya contamos con otra zona de búsqueda directa.

![imagen23](./images/servidor_web_basico/23.png)

Ahora tenemos que añadir un nuevo registro.

![imagen24](./images/servidor_web_basico/24.png)

![imagen25](./images/servidor_web_basico/25.png)

Accedemos ahora desde W10 a la misma página mediante el nombre principal del dominio y desde cualquier otro alias que haya sido definido en la configuración DNS.

![imagen26](./images/servidor_web_basico/26.png)

Tratamos de acceder desde W10 al sitio www del dominio principal.

![imagen27](./images/servidor_web_basico/27.png)

Lo que nos ocurre es que nos da un error porque el alias de www no esta creado en la configuración DNS.

Añadimos un alias en el servicio DNS que relacione el sitio www con el dominio principal.

![imagen28](./images/servidor_web_basico/28.png)

![imagen29](./images/servidor_web_basico/29.png)

![imagen30](./images/servidor_web_basico/30.png)

Intentamos ahora acceder desde W10 a www.

![imagen31](./images/servidor_web_basico/31.png)

Creamos una página web HTML sencilla (index.htm) como página principal de mi dominio y la colocamos en `C:\Inetpub\wwwroot`.

![imagen32](./images/servidor_web_basico/32.png)

![imagen33](./images/servidor_web_basico/33.png)

Comprobamos el acceso a esta página desde el propio Servidor y desde el Cliente, utilizando los diferentes alias y direcciones configurados en el servicio DNS.

* Servidor.

![imagen34](./images/servidor_web_basico/34.png)

![imagen35](./images/servidor_web_basico/35.png)

* Cliente.

![imagen36](./images/servidor_web_basico/36.png)

![imagen37](./images/servidor_web_basico/37.png)

Creamos un pequeño sitio web con varias páginas e imágenes organizadas en subcarpetas de wwwroot.

![imagen38](./images/servidor_web_basico/38.png)

![imagen39](./images/servidor_web_basico/39.png)

![imagen40](./images/servidor_web_basico/40.png)

![imagen41](./images/servidor_web_basico/41.png)

![imagen42](./images/servidor_web_basico/42.png)

Accedemos y navegamos por los sitios web tanto desde el Servidor como desde el Cliente W10.

* Servidor.

![imagen43](./images/servidor_web_basico/43.png)

![imagen44](./images/servidor_web_basico/44.png)

![imagen45](./images/servidor_web_basico/45.png)

![imagen46](./images/servidor_web_basico/46.png)

* Cliente.

![imagen47](./images/servidor_web_basico/47.png)

![imagen48](./images/servidor_web_basico/48.png)

![imagen49](./images/servidor_web_basico/49.png)

![imagen50](./images/servidor_web_basico/50.png)

---

## **2. Creación De Sitios Web Independientes.**

Ahora en la configuración DNS creamos una nueva zona de búsqueda directa, dentro de aquí creamos un dominio y varios alias.

![imagen51](./images/servidor_web_basico/51.png)

Creamos una zona de búsqueda directa.

![imagen52](./images/servidor_web_basico/52.png)

Nos sale el asistente para la nueva zona.

![imagen53](./images/servidor_web_basico/53.png)

Elegimos el tipo de zona que queremos.

![imagen54](./images/servidor_web_basico/54.png)

Seleccionamos que queremos que se repliquen los datos para todos los servidores DNS que se ejecutan en controladores de dominio en el dominio que tengo.

![imagen55](./images/servidor_web_basico/55.png)

Le ponemos un nombre a nuestra zona.

![imagen56](./images/servidor_web_basico/56.png)

Permitimos actualizaciones dinámicas seguras.

![imagen57](./images/servidor_web_basico/57.png)

Se ha creado la nueva zona.

![imagen58](./images/servidor_web_basico/58.png)

Ya contamos con otra zona de búsqueda directa.

![imagen59](./images/servidor_web_basico/59.png)

Ahora tenemos que añadir unos nuevos registros.

![imagen60](./images/servidor_web_basico/60.png)

![imagen61](./images/servidor_web_basico/61.png)

![imagen62](./images/servidor_web_basico/62.png)

![imagen63](./images/servidor_web_basico/63.png)

![imagen64](./images/servidor_web_basico/64.png)

![imagen65](./images/servidor_web_basico/65.png)

Creamos dos nuevos sitios web, uno asociado al dominio principal y otro a un subdominio, estos dos sitios webs serán independientes.

![imagen66](./images/servidor_web_basico/66.png)

![imagen67](./images/servidor_web_basico/67.png)

![imagen68](./images/servidor_web_basico/68.png)

![imagen69](./images/servidor_web_basico/69.png)

![imagen70](./images/servidor_web_basico/70.png)

![imagen71](./images/servidor_web_basico/71.png)

Finalmente, incorporamos algunos archivos HTML, imágenes y subcarpetas a mi nuevo sitio web y comprobamos el acceso desde navegadores web tanto del Servidor como del Cliente W10.

![imagen72](./images/servidor_web_basico/72.png)

![imagen73](./images/servidor_web_basico/73.png)

---

## **3. Creación De Directorios Virtuales.**

Creamos un directorio virtual, de una carpeta que hemos creado anteriormente.

![imagen74](./images/servidor_web_basico/74.png)

![imagen75](./images/servidor_web_basico/75.png)

![imagen76](./images/servidor_web_basico/76.png)

![imagen77](./images/servidor_web_basico/77.png)

Este directorio virtual debe contener, al menos, tres subcarpetas con páginas html diferentes para comprobar el buen funcionamiento del sitio.

![imagen78](./images/servidor_web_basico/78.png)

![imagen79](./images/servidor_web_basico/79.png)

![imagen80](./images/servidor_web_basico/80.png)

![imagen81](./images/servidor_web_basico/81.png)

![imagen82](./images/servidor_web_basico/82.png)

![imagen83](./images/servidor_web_basico/83.png)

![imagen84](./images/servidor_web_basico/84.png)

![imagen85](./images/servidor_web_basico/85.png)

Habilitamos dentro de nuestro directorio virtual para poder acceder a este directorio desde un navegador web.

![imagen86](./images/servidor_web_basico/86.png)

Comprobamos el acceso a cada una de las diferentes secciones de nuestro sitio web, tanto desde el Servidor como desde el Cliente W10.

* Servidor.

![imagen87](./images/servidor_web_basico/87.png)

![imagen88](./images/servidor_web_basico/88.png)

![imagen89](./images/servidor_web_basico/89.png)

![imagen90](./images/servidor_web_basico/90.png)

* Cliente.

![imagen91](./images/servidor_web_basico/91.png)

![imagen92](./images/servidor_web_basico/92.png)

![imagen93](./images/servidor_web_basico/93.png)

![imagen94](./images/servidor_web_basico/94.png)

---
