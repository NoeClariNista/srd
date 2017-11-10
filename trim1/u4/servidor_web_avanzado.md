___

# **Instalación Y Configuración De Un Servidor Web Avanzado.**

---

## **Carpetas Seguras.**

// * Creamos una nueva zona de búsqueda directa en los servicios DNS asociado al dominio miEmpresa. Creamos también una carpeta miEmpresa en C:\ y una subcarpeta ‘principal’.

// * Crea  un  nuevo  sitio  web  denominado  
miEmpresa   en  IIS  asociado  a  la  subcarpeta  anterior  y  con  acceso a través de la dirección www.miEmpresa.com. Actualiza DNS adecuadamente.

// * Siguiendo los  pasos  detallados  en  el  documento  PDF  de  Carpetas  Seguras  y  Privadas,  crea  un  nuevo  
sitio web (denominado ‘pagos’) como subdominio de
miEmpresa (pagos.miEmpresa.com) y configura este último para ser accedido de forma segura, vía ‘https’.

* Crea el sitio web, asociado a una carpeta (miEmpresa\pagos) y con la configuración adecuada en IIS y en los servicios DNS. Comprueba el acceso (aún vía ‘http’) con un navegador desde el propio servidor y desde un cliente W10.

o Configuración  A:  Siguiendo  los  pasos  del  tutorial correspondiente,  configura  el  nuevo  sitio  para  
que se pueda acceder (sólo) como sitio web seguro (https) con un Certificado Autofirmado.

o Configuración B:  Crearemos un nuevo sitio seguro (tienda.miempresa.com) con la generación de un  Certificado  Digital a  través  de  la  aplicación  OpenSSL.  Para  empezar,  realizaremos  la  solicitud  de un nuevo certificado de servidor para nuestro sitio seguro (crear fichero certreq.txt).

o Descargar e instalar OpenSSL para Windows.
o A través de OpenSSl genera un nuevo certificad
o de servidor, siguiendo los pasos que se detallan
en tutorial web (y comprobando los ficheros generados en cada paso): generar una clave privada
de  la  entidad  certificadora,  crear  un  certificado  digital  de  la  entidad  certificadora  y,  finalmente,  

crear un certificado digital de nuestra web.
o Importar  el  nuevo  certificado  de  servidor  creado  para  completar  la  petición  pendiente  en  
nuestro sitio seguro ‘
pagos’
.

* Requerir  que  nuestros  sitio  seguros  sólo  se  pueda  acceder  mediante  una  conexión  segura  y  
reiniciar lo
s sitios web.

* Finalmente, acceder mediante http y mediante https a los sitios seguros desde el propio servidor y
desde un cliente W7, aceptando los posibles problemas con la entidad certificadora.
