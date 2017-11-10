___

# **Servidor Web Básico.**
___

## **Internet Information Server – Instalación, Configuración Y Creación De Sitios Web.**

Instalar  IIS  en  Windows  2012  Server  (Asistente  para  configurar  servidor  

  Servidor  de  
Aplicaciones IIS). Incluir Autenticación Básica y de Windows.
•
Comprobar  acceso  a  nuestro  servidor  web  (localhost)  desde  un  navegador  web  (debe  
aparecer una página en construcción).
•
Entrar en cliente Windows 7 y acceder, desde un navegador web,  a la página principal del
servidor a t
ravés de la IP del servidor.
•
Acceder  ahora  desde  W7  a  la  misma  página  mediante  el  nombre  principal  del  dominio  y  
desde cualquier otro alias que haya sido definido en la configuración DNS.
•
Tratar  de  acceder  desde  W7  al  sitio  www  del  dominio  principal.  ¿Qué  ocurre?  Añade  un  
alias en el servicio DNS que relacione el sitio www con el dominio principal. Intenta ahora
acceder desde W7.
•
Crea  una  página  web  HTML  sencilla  (index.htm)  como  página  principal  de  tu  dominio  y  
colócala  en  C:
\Inetpub\
wwwroot.  Comprueba  el  acceso  a  esta  página  desde  el  propio  
servidor  y  desde  el  cliente,  utilizando  los  diferentes  alias  y  direcciones  configurados  en  el  
servicio DNS.
•
Crea  un  pequeño  sitio  web  con  varias  páginas  e  imágenes  organizadas  en  subcarpetas  de  
wwwroot.   Abre   el   Administ
rador   de   Internet   Information   Services   y   comprueba   la   
estructura del sitio creado en Sitio Web Predeterminado. Accede y navega por el sitio web
tanto desde el servidor como desde el cliente W7.

---

## **Internet Information Server – Creación De Sitios Web Independientes.**

Siguiendo  los  pasos  detallados  en  el  documento  PDF  de  Instalación  y  Configuración  IIS,  
apartado  2  sobre  creación  de  sitios  web  independientes,  crea  dos  nuevos  sitios  web,  uno  
asociado al dominio principal y otro a un subdominio.
•
Puedes  utilizar  las  sugerencias  (en  cuanto  a  dominios,  subdominios,  carpetas,  ficheros,  
etc.)  incluidas  en  el  citado  documento  o,  aún  mejor,  definir  tu  propio  sitio  web  con  algún  
tema que te interese. Ejemplos para los dos sitios: srd.edu / recursos.srd.edu
•
Sería  especialmente  interesante  la  opción  de  que  el  nuevo  sitio  web  no  fuera  parte  de  tu  
dominio  principal  de  W2008  Server,  sino  que  crearas  un  nuevo  do
minio  para  este  sitio  
web. Recuerda que para esto sería necesario, además de todos los pasos de configuración
de  IIS,  incluir  una  nueva  zona  de  búsqueda  directa  en  tu  servicio  DNS  con  las  opciones  de  
configuración necesarias (registros A, CNAME, ...)
•
Finalme
nte,  incorpora  algunos  archivos  HTML,  imágenes  y  subcarpetas  a  tu  nuevo  sitio  
web  y  comprueba  el  acceso  desde  navegadores  web  tanto  del  servidor  como  del  cliente  
W7.

---

## **Internet Information Server – Creación De Directorios Virtuales.**

Siguiendo  los  pasos  detallados  en  el  documento  PDF  de  Instalación  y  Configuración  IIS,  
apartado  3  sobre  creación  de  directorios  virtuales,  crea  una  carpeta  que  se  corresponda  
con una posible sección del sitio web creado en la práctica anterior (creación de sitios web
independientes).  Crea  un  nuevo  directorio  virtual  en  IIS  (dentro  del  citado  sitio  web)  y  
relaciónalo con la carpeta que has cre
ado.
•
Este   directorio   virtual   debe   contener,   al   menos,   tres   subcarpetas   con   páginas   html   
diferentes  para  comprobar  el  buen  funcionamiento  del  sitio.  Por  ejemplo,  tu  directorio  
virtual  podría  ser  
departamentos
,  con  tres  subcarpetas  
contabilidad
,
administraci
ón
  e
informática
 y acceso a través de la URL
servicios.srd.edu
 o
departamentos.srd.edu
•
Comprobar  el  acceso  a  cada  una  de  las  diferentes  secciones  de  nuestro  sitio  web,  tanto  
desde el servidor como desde el cliente W7.
•
Recuerda realizar las configuraciones
DNS necesarias para que los diferentes nombres que
se han ido creando referentes a nuestro sitio web sean resueltos correctamente.
•
Finalmente,  elige  los  documentos  que  serán  mostrados  por  defecto  en  cada  uno  de  los  
sitios y directorios virtuales creados y el orden de prioridad entre ellos.

---
