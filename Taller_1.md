# GLOSARIO HTTP

1. *Request*: Es el acceso o "hit" que requiere un navegador cuando realiza una peticion de un objeto web(imagen,html,script,etc)
[Fuente](http://www.alegsa.com.ar/Dic/request.php)

2. *Response*: Se utiliza para presentar en la pantalla del navegador del usuario el resultado de cualquier código creado.
[Fuente](https://www.uv.es/~jac/guia/asp/asp10.htm)

3. *Status Codes*: Los codigos de estado de respuesta HTTP, son los indicadores de si se ha completado satisfactoriamente una solicitud de HTTP especifica. Estas se agrupan en cinco clases: respuestas informativas, satisfactorias, redirecciones, errores de los clientes y errores de los servidores.
[Fuente](https://developer.mozilla.org/es/docs/Web/HTTP/Status)

4. *Methods*:
    - GET: Se utiliza para recuperar información del servidor dado utilizando un URL determinado.
    - POST: Se utiliza para enviar datos al servidor;como la carga de archivos, información del cliente, etc.
    - HEAD: Se utiliza para transferir la linea de estado y la seccion del encabezado.
    - OPTIONS: Describe las opciones de comunicación para el recurso objetivo.
    - PUT: Reemplaza todas las representaciones actuales del recurso de destino con el contenido cargado.
    - DELETE: Elimina todas las representaciones actuales del recurso del destino dado por un URI.
[Fuente](https://www.tutorialspoint.com/http/http_methods.htm)

5. *Header*: Son los parametros que se envian en una petición o respuesta de HTTP al cliente o al servidor para proporcionar información.
    - Accept: Tipos de contenido que se aceptan.
    - Accept-Charset: Conjunto de caracteres que se aceptan.
    - Accept-Encoding: Lista de codificaciones que se aceptan.
    - Cache-Control: Se controlan las politicas de cache.
    - Connection: Se controla el tipo de conección.
    - Cookie: Una cookie enviada anteriormente por el servidor.
    - Set-Cookie: Envia las cookies.
    - Host: El nombre de dominio o dirección IP.
    - Origin: Inicia una petición para servidores con respuesta Access Control.
    - Referer: Indica la dirección URL de donde proviene.
    - User-Agent: Contiene la información de la petición, como el navegador, sistema operativo,etc.
    - Content-Encoding: Es usada para comprimir el media-type.
    - Content-Lenght: El tamaño del contenido de la petición en byte.
    - Content-Type: El tipo de contenido de la petición en POST o PUT.
    - Location: Proporciona la informacion de la ubicacion de un recurso recién creado.
    - Upgrade: Pide al servidor que que se actualice la versión de HTTP para funcionar.
[Fuente](https://es.wikipedia.org/wiki/Anexo:Cabeceras_HTTP)

# Tabla de RES/REQ de (htttp://www.inf.ucv.cl/~ifigueroa)

| REQ/RES | Método HTTP | URL                                                                                                   | Headers                                                                                                                                                                  | Status | Descripción                                       |
|---------|-------------|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|---------------------------------------------------|
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/doku.php                                                            | Upgrade-Insecure-Requests, User-Agent,Accept                                                                                                                             | n/a    | Petición inicial del sitio                        |
| RES     | n/a         | n/a                                                                                                   | Date,Server,X-Powered-By Expires,Cache-Control Pragma,X-UA-Compatible Vary,Content-Encoding Content-Length,Keep-Alive Connection,Content-Type                            | 200    | Se devuelve correctamente al sitio.               |
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/lib/tpl/bootstrap3/assets/bootstrap/default/bootstrap.min.css       | User-Agent,Accept                                                                                                                                                        |        | Carga un archivo css.                             |
| RES     | n/a         | n/a                                                                                                   | Date,Server Last-Modified,ETag Accept-Ranges,Vary Content-Encoding Content-Length Content-Type                                                                           | 200    | Abre correctamente el archivo.                    |
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/lib/exe/css.php?t=bootstrap3&tseed=44b1422730da0b8e0624124cac9afe4b | User-Agent,Accept                                                                                                                                                        |        | Carga un archivo css.                             |
| RES     | n/a         | n/a                                                                                                   | Date,Server X-Powered-By Cache-Control,Pragma ETag,Vary Content-Encoding Content-Length Content-Type                                                                     | 200    | Abre correctamente el archivo que contiene texto. |
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/lib/tpl/bootstrap3/assets/font-awesome/css/font-awesome.min.css     | User-Agent,Accept                                                                                                                                                        |        | Carga un archivo css.                             |
| RES     | n/a         | n/a                                                                                                   | Date,Server Last-Modified,ETag Accept-Ranges,Vary Accept-Encoding Content-Encoding Content-Length Content-Type                                                           | 200    | Abre correctamente el archivo.                    |
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/lib/exe/indexer.php?id=start&1554231749                             | User-Agent,Accept                                                                                                                                                        |        | Carga una imagen.                                 |
| RES     | n/a         | n/a                                                                                                   | Date,Server X-Powered-By,Expires Cache-Control,Pragma Connection Content-Length Content-Type                                                                             | 200    | Abre correctamente la imagen/gif                  |
| REQ     | GET         | http://zeus.inf.ucv.cl/~ifigueroa/lib/tpl/bootstrap3/images/favicon.ico                               | User-Agent,Accept                                                                                                                                                        |        | Carga una imagen.                                 |
| RES     | n/a         | n/a                                                                                                   | Date,Server Last-Modified,ETag Accept-Ranges Content-Lengtheep-Alive Connection: Keep-Alive Content-Type                                                                 | 200    | Abre correctamente la imagen.                     |
| REQ     | GET         | https://www.youtube.com/sw.js                                                                         | User-Agent,Accept Service-Worker                                                                                                                                         |        | Carga un enlace a youtube                         |
| RES     | n/a         | n/a                                                                                                   | content-type,content-encoding expires,cache-control x-content-type-options content-length strict-transport-security x-frame-options,date server,x-xss-protection alt-svc | 200    | Abre el enlace.                                   |
| REQ     | GET         | http://prodavmoodle.ucv.cl/pluginfile.php/810329/mod_resource/content/1/1%20-%20Taller%20HTTP.pdf     | Upgrade-Insecure-Requests User-Agent,Accept                                                                                                                              |        | Carga un archivo pdf.                             |
| RES     | n/a         | n/a                                                                                                   | Server,Date Content-Type Content-Length X-Powered-By Content-Disposition Cache-Control Expires,Pragma  Etag,Last-Modified Accept-Ranges                                  | 200    | Abre un archivo pdf.                              |
*Se muestra el inicio del sitio.


# Sitio Web de mi agrado (https://www.youtube.com/?hl=es-419&gl=CL)
| REQ/RES | Método HTTP | URL                                                                                                      | Headers                                                                                                                                                                                                        | Status | Descripción                            |
|---------|-------------|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|----------------------------------------|
| REQ     | POST        | https://www.youtube.com/youtubei/v1/log_event?alt=json&key=AIzaSyAO_FJ2SlqU8Q4STEHLGCilw_Y9_11qcW8       | Origin,X-YouTube-Page-Label User-Agent  X-YouTube-Variants-Checksum Content-Type,X-YouTube-Page-CL X-YouTube-Utc-Offset X-YouTube-Client-Name X-YouTube-Client-Version X-Goog-Visitor-Id,Accept                | n/a    | Petición inicial del sitio.            |
| RES     | n/a         | n/a                                                                                                      | content-type,vary content-encoding date,server cache-control content-length x-xss-protection x-frame-options x-content-type-options alt-svc                                                                    | 200    | Se devuelve correctamente al sitio.    |
| REQ     | GET         | https://www.youtube.com/?hl=es-419&gl=CL                                                                 | Upgrade-Insecure-Requests User-Agent,Accept                                                                                                                                                                    | n/a    | Peticion de carga de inicio del sitio. |
| RES     | n/a         | n/a                                                                                                      | x-content-type-options content-encoding,p3p expires strict-transport-security cache-control,content-type x-frame-options date,server x-xss-protection,alt-svc                                                  | 200    | Se devuelve correctamente al inicio.   |
| REQ     | GET         | https://www.youtube.com/yts/jsbin/web-animations-next-lite.min-vflluX5aW/web-animations-next-lite.min.js | User-Agent,Accept                                                                                                                                                                                              | n/a    | Peticion de archivo javascript.        |
| RES     | n/a         | n/a                                                                                                      | accept-ranges,content-encoding content-type timing-allow-origin content-length,date expires,last-modified x-content-type-options server,x-xss-protection cache-control,age,alt-svc                             | 200    | Se muestra correctamente el archivo.   |
| REQ     | GET         | https://www.youtube.com/yts/htmlbin/desktop_polymer_sel_auto_svg_home-vflAmqykD.html                     | Origin,User-Agent Accept                                                                                                                                                                                       | n/a    | Peticion archivo html.                 |
| RES     | n/a         | n/a                                                                                                      | accept-ranges,content-encoding content-type access-control-allow-origin timing-allow-origin content-length,date expires last-modified x-content-type-options,server x-xss-protection,cache-control age,alt-svc | 200    | Abre correctamente archivo html.       |
| REQ     | GET         | https://www.youtube.com/yts/jsbin/scheduler-vflWUk-ha/scheduler.js                                       | User-Agent,Accept                                                                                                                                                                                              | n/a    | Peticion de archivo javascript.        |
| RES     | n/a         | n/a                                                                                                      | accept-ranges,content-encoding content-type,timing-allow-origin content-length,date expires,last-modified x-content-type-options,server x-xss-protection,cache-control age,alt-svc                             | 200    | Se muestra correctamente el archivo.   |

*Carga de sitio inicial youtube Chile.