___

# **Servidor Web Básico.**
___

## **Instalación, Configuración Y Creación De Sitios Web.**

Instalamos IIS en Windows 2012 Server (Asistente para Configurar Servidor, Servidor de Aplicaciones IIS). Incluimos Autenticación Básica y de Windows.

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

Finalmente terminamos la instalación del IIS en Windows 2012 Server.

![imagen13](./images/servidor_web_basico/13.png)

Ahora comprobamos el acceso a nuestro Servidor Web (localhost) desde un navegador web (debe aparecer una página en construcción).

![imagen14](./images/servidor_web_basico/14.png)

Entramos en el Cliente Windows 10 y accedemos, desde un navegador web, a la página principal del Servidor a través de la IP del Servidor.

![imagen15](./images/servidor_web_basico/15.png)

Ahora en la configuración DNS creamos una nueva zona de búsqueda directa, dentro de aqui creamos un dominio y un alias..

![imagen16](./images/servidor_web_basico/16.png)

![imagen17](./images/servidor_web_basico/17.png)

![imagen18](./images/servidor_web_basico/18.png)

![imagen19](./images/servidor_web_basico/19.png)

![imagen20](./images/servidor_web_basico/20.png)

![imagen21](./images/servidor_web_basico/21.png)

![imagen22](./images/servidor_web_basico/22.png)

![imagen23](./images/servidor_web_basico/23.png)

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

Intentamos ahora acceder desde W10.

![imagen31](./images/servidor_web_basico/31.png)

Creamos una página web HTML sencilla (index.htm) como página principal de mi dominio y la colocamos en C:\Inetpub\wwwroot.

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

Accedemos y navegamos por el sitio web tanto desde el Servidor como desde el Cliente W10.

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

## **Creación De Sitios Web Independientes.**

Ahora en la configuración DNS creamos una nueva zona de búsqueda directa, dentro de aqui creamos un dominio y varios alias.

![imagen51](./images/servidor_web_basico/51.png)

![imagen52](./images/servidor_web_basico/52.png)

![imagen53](./images/servidor_web_basico/53.png)

![imagen54](./images/servidor_web_basico/54.png)

![imagen55](./images/servidor_web_basico/55.png)

![imagen56](./images/servidor_web_basico/56.png)

![imagen57](./images/servidor_web_basico/57.png)

![imagen58](./images/servidor_web_basico/58.png)

![imagen59](./images/servidor_web_basico/59.png)

![imagen60](./images/servidor_web_basico/60.png)

![imagen61](./images/servidor_web_basico/61.png)

![imagen62](./images/servidor_web_basico/62.png)

![imagen63](./images/servidor_web_basico/63.png)

![imagen64](./images/servidor_web_basico/64.png)

![imagen65](./images/servidor_web_basico/65.png)

![imagen66](./images/servidor_web_basico/66.png)

Creamos dos nuevos sitios web, uno asociado al dominio principal y otro a un subdominio, estos dos sitios webs seran independientes.

![imagen67](./images/servidor_web_basico/67.png)

![imagen68](./images/servidor_web_basico/68.png)

![imagen69](./images/servidor_web_basico/69.png)

![imagen70](./images/servidor_web_basico/70.png)

![imagen71](./images/servidor_web_basico/71.png)

![imagen72](./images/servidor_web_basico/72.png)

Finalmente, incorporamos algunos archivos HTML, imágenes y subcarpetas a mi nuevo sitio web y comprobamos el acceso desde navegadores web tanto del Servidor como del Cliente W10.

![imagen73](./images/servidor_web_basico/73.png)

![imagen74](./images/servidor_web_basico/74.png)

---

## **Creación De Directorios Virtuales.**

Siguiendo  los  pasos  detallados  en  el  documento  PDF  de  Instalación  y  Configuración  IIS,  
apartado  3  sobre  creación  de  directorios  virtuales,  crea  una  carpeta  que  se  corresponda  
con una posible sección del sitio web creado en la práctica anterior (creación de sitios web
independientes).  Crea  un  nuevo  directorio  virtual  en  IIS  (dentro  del  citado  sitio  web)  y  
relaciónalo con la carpeta que has cre
ado.

* Este directorio virtual debe contener, al menos, tres subcarpetas con páginas html diferentes para  comprobar el buen funcionamiento del sitio. Por ejemplo, tu directorio virtual podría ser departamentos, con tres subcarpetas contabilidad, administración  e informática y acceso a través de la URL servicios.srd.edu o departamentos.srd.edu.

![imagen01](./images/servidor_web_basico/01.png)

* Comprobamos el acceso a cada una de las diferentes secciones de nuestro sitio web, tanto desde el Servidor como desde el Cliente W10.

![imagen01](./images/servidor_web_basico/01.png)

* Recuerda realizar las configuraciones DNS necesarias para que los diferentes nombres que se han ido creando referentes a nuestro sitio web sean resueltos correctamente.

![imagen01](./images/servidor_web_basico/01.png)

* Finalmente, elige los documentos que serán mostrados por defecto en cada uno de los sitios y directorios virtuales creados y el orden de prioridad entre ellos.

![imagen01](./images/servidor_web_basico/01.png)

---
