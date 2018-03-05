___

>Trabajo Realizado Por:
>
>* Noelia Hernández Domínguez.
>
>* Omar Hernández Padrón.

___

# **Instalación Y Configuración Del Servicio VoIP En Windows 2012 Server.**

---

Instalamos y configuramos un Servidor y un Cliente para establecer comunicaciones de Voz mediante el Servicio VoIP (Voice Over Internet Protocol) sobre sistemas Windows.

En el Servidor nos registramos, descargamos e instalamos el software para central PBX 3CX Phone System.

Vamos a la página oficial de [3xc](http://www.3cx.es)

![imagen01](./images/instalacion_y_configuracion_servidor_voip_windows/01.png)

Nos registramos.

![imagen02](./images/instalacion_y_configuracion_servidor_voip_windows/02.png)

Descargamos PBX 3CX Phone System.

![imagen03](./images/instalacion_y_configuracion_servidor_voip_windows/03.png)

Empezamos la instalación del PBX 3CX Phone System.

![imagen04](./images/instalacion_y_configuracion_servidor_voip_windows/04.png)

Para la instalación del Servidor PBX se necesita .NET Framework 4.6.1.

![imagen05](./images/instalacion_y_configuracion_servidor_voip_windows/05.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen06](./images/instalacion_y_configuracion_servidor_voip_windows/06.png)

![imagen07](./images/instalacion_y_configuracion_servidor_voip_windows/07.png)

![imagen08](./images/instalacion_y_configuracion_servidor_voip_windows/08.png)

![imagen09](./images/instalacion_y_configuracion_servidor_voip_windows/09.png)

![imagen10](./images/instalacion_y_configuracion_servidor_voip_windows/10.png)

![imagen11](./images/instalacion_y_configuracion_servidor_voip_windows/11.png)

Reiniciamos la máquina virtual para poder completar la instalación de .NET Framework.

![imagen12](./images/instalacion_y_configuracion_servidor_voip_windows/12.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen13](./images/instalacion_y_configuracion_servidor_voip_windows/13.png)

![imagen14](./images/instalacion_y_configuracion_servidor_voip_windows/14.png)

![imagen15](./images/instalacion_y_configuracion_servidor_voip_windows/15.png)

![imagen16](./images/instalacion_y_configuracion_servidor_voip_windows/16.png)

![imagen17](./images/instalacion_y_configuracion_servidor_voip_windows/17.png)

![imagen18](./images/instalacion_y_configuracion_servidor_voip_windows/18.png)

![imagen19](./images/instalacion_y_configuracion_servidor_voip_windows/19.png)

Para la instalación del servidor PBX se necesitan Microsoft Visual C++ 2008 Redistributable, Microsoft Visual C++ 2010 Redistributable x64 y Microsoft Visual C++ 2015 Redistributable (x64).

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen20](./images/instalacion_y_configuracion_servidor_voip_windows/20.png)

![imagen21](./images/instalacion_y_configuracion_servidor_voip_windows/21.png)

![imagen22](./images/instalacion_y_configuracion_servidor_voip_windows/22.png)

![imagen23](./images/instalacion_y_configuracion_servidor_voip_windows/23.png)

![imagen24](./images/instalacion_y_configuracion_servidor_voip_windows/24.png)

![imagen25](./images/instalacion_y_configuracion_servidor_voip_windows/25.png)

![imagen26](./images/instalacion_y_configuracion_servidor_voip_windows/26.png)

![imagen27](./images/instalacion_y_configuracion_servidor_voip_windows/27.png)

![imagen28](./images/instalacion_y_configuracion_servidor_voip_windows/28.png)

![imagen29](./images/instalacion_y_configuracion_servidor_voip_windows/29.png)

![imagen30](./images/instalacion_y_configuracion_servidor_voip_windows/30.png)

Finalmente ya se nos instalará el PBX 3CX Phone System.

![imagen31](./images/instalacion_y_configuracion_servidor_voip_windows/31.png)

Iniciamos el panel de control, para ello elegimos la opción 1, y realizamos las siguientes acciones de configuración.

![imagen32](./images/instalacion_y_configuracion_servidor_voip_windows/32.png)

Ponemos la clave de la licencia que se nos mando por correo después de registrarnos.

![imagen33](./images/instalacion_y_configuracion_servidor_voip_windows/33.png)

Añadimos un usuario y su contraseña.

![imagen34](./images/instalacion_y_configuracion_servidor_voip_windows/34.png)

Añadimos una clave pública.

![imagen35](./images/instalacion_y_configuracion_servidor_voip_windows/35.png)

Decimos que la IP pública es estática.

![imagen36](./images/instalacion_y_configuracion_servidor_voip_windows/36.png)

Seleccionamos nuestro subdominio.

![imagen37](./images/instalacion_y_configuracion_servidor_voip_windows/37.png)

Seleccionamos los puertos para poder acceder a nuestro panel de control.

![imagen38](./images/instalacion_y_configuracion_servidor_voip_windows/38.png)

Añadimos una IP local.

![imagen39](./images/instalacion_y_configuracion_servidor_voip_windows/39.png)

Esperamos que carguen los datos.

![imagen40](./images/instalacion_y_configuracion_servidor_voip_windows/40.png)

Seleccionamos extensiones de 3 dígitos.

![imagen41](./images/instalacion_y_configuracion_servidor_voip_windows/41.png)

Añadimos el correo electrónico del administrador.

![imagen42](./images/instalacion_y_configuracion_servidor_voip_windows/42.png)

Seleccionamos la configuración regional adecuada.

![imagen43](./images/instalacion_y_configuracion_servidor_voip_windows/43.png)

Creamos una extensión, del usuario operador.

![imagen44](./images/instalacion_y_configuracion_servidor_voip_windows/44.png)

Seleccionamos los países con los que se podrá establecer comunicaciones.

![imagen45](./images/instalacion_y_configuracion_servidor_voip_windows/45.png)

Seleccionamos el idioma.

![imagen46](./images/instalacion_y_configuracion_servidor_voip_windows/46.png)

Confirmamos los datos de registro.

![imagen47](./images/instalacion_y_configuracion_servidor_voip_windows/47.png)

Esperamos que se cree todo en la base de datos.

![imagen48](./images/instalacion_y_configuracion_servidor_voip_windows/48.png)

![imagen49](./images/instalacion_y_configuracion_servidor_voip_windows/49.png)

Finalmente ya tenemos creado el panel de control del 3CX.

![imagen50](./images/instalacion_y_configuracion_servidor_voip_windows/50.png)

Entramos a nuestro panel de control poniendo nuestras credenciales.

![imagen51](./images/instalacion_y_configuracion_servidor_voip_windows/51.png)

Vemos todo los datos en nuestro panel de control.

![imagen52](./images/instalacion_y_configuracion_servidor_voip_windows/52.png)

Creamos tres extensiones correspondientes a diferentes usuarios con toda su información.

![imagen53](./images/instalacion_y_configuracion_servidor_voip_windows/53.png)

* lia.

![imagen54](./images/instalacion_y_configuracion_servidor_voip_windows/54.png)

![imagen55](./images/instalacion_y_configuracion_servidor_voip_windows/55.png)

![imagen56](./images/instalacion_y_configuracion_servidor_voip_windows/56.png)

* noe.

![imagen57](./images/instalacion_y_configuracion_servidor_voip_windows/57.png)

![imagen58](./images/instalacion_y_configuracion_servidor_voip_windows/58.png)

![imagen59](./images/instalacion_y_configuracion_servidor_voip_windows/59.png)

* noeclarinista.

![imagen60](./images/instalacion_y_configuracion_servidor_voip_windows/60.png)

![imagen61](./images/instalacion_y_configuracion_servidor_voip_windows/61.png)

![imagen62](./images/instalacion_y_configuracion_servidor_voip_windows/62.png)

Ya tenemos las tres extensiones creadas.

![imagen63](./images/instalacion_y_configuracion_servidor_voip_windows/63.png)

Nos descargamos e instalamos el SIP softphone 3CX Phone.

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen64](./images/instalacion_y_configuracion_servidor_voip_windows/64.png)

![imagen65](./images/instalacion_y_configuracion_servidor_voip_windows/65.png)

![imagen66](./images/instalacion_y_configuracion_servidor_voip_windows/66.png)

![imagen67](./images/instalacion_y_configuracion_servidor_voip_windows/67.png)

![imagen68](./images/instalacion_y_configuracion_servidor_voip_windows/68.png)

![imagen69](./images/instalacion_y_configuracion_servidor_voip_windows/69.png)

En el Cliente Windows 10 descargamos e instalamos el software SIP softphone 3CX Phone for Windows.

![imagen70](./images/instalacion_y_configuracion_servidor_voip_windows/70.png)

Los pasos de la instalación los realizamos como se pueden ver en las siguientes imágenes.

![imagen71](./images/instalacion_y_configuracion_servidor_voip_windows/71.png)

![imagen72](./images/instalacion_y_configuracion_servidor_voip_windows/72.png)

![imagen73](./images/instalacion_y_configuracion_servidor_voip_windows/73.png)

![imagen74](./images/instalacion_y_configuracion_servidor_voip_windows/74.png)

![imagen75](./images/instalacion_y_configuracion_servidor_voip_windows/75.png)

![imagen76](./images/instalacion_y_configuracion_servidor_voip_windows/76.png)

* Servidor  y  Clientes:  Realizar  la  instalación  y  configuración  completa  del  3CX Phone   siguiendo  las  los  enlaces  y  manuales  tanto  en  el  servidor  como  en   los clientes  con  el  fin  de  establecer  una  comunicación  interna  de  voz  entre  los  
usuarios.  Crear las cuentas correspondientes a los usuarios en cada terminal.

![imagen77](./images/instalacion_y_configuracion_servidor_voip_windows/77.png)

![imagen78](./images/instalacion_y_configuracion_servidor_voip_windows/78.png)

![imagen79](./images/instalacion_y_configuracion_servidor_voip_windows/79.png)

![imagen80](./images/instalacion_y_configuracion_servidor_voip_windows/80.png)

![imagen81](./images/instalacion_y_configuracion_servidor_voip_windows/81.png)

![imagen82](./images/instalacion_y_configuracion_servidor_voip_windows/82.png)

![imagen83](./images/instalacion_y_configuracion_servidor_voip_windows/83.png)

![imagen84](./images/instalacion_y_configuracion_servidor_voip_windows/84.png)

![imagen85](./images/instalacion_y_configuracion_servidor_voip_windows/85.png)

![imagen86](./images/instalacion_y_configuracion_servidor_voip_windows/86.png)

![imagen87](./images/instalacion_y_configuracion_servidor_voip_windows/87.png)

![imagen88](./images/instalacion_y_configuracion_servidor_voip_windows/88.png)

Efectuamos llamadas entre los usuarios correspondientes a las extensiones creadas en el Servidor.

* Extensión 001 llama a extensión 002.

![imagen89](./images/instalacion_y_configuracion_servidor_voip_windows/89.png)

![imagen90](./images/instalacion_y_configuracion_servidor_voip_windows/90.png)

* Extensión 002 llama a extensión 001.

![imagen91](./images/instalacion_y_configuracion_servidor_voip_windows/91.png)

![imagen92](./images/instalacion_y_configuracion_servidor_voip_windows/92.png)

---
