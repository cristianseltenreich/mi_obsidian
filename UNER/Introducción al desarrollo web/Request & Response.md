● La estructura de los mensajes es la misma para request y response. 
![[Pasted image 20240329191455.png]]

● Dos ejemplos de mensajes HTTP. Los saltos de línea son importantes por lo que se muestran en rojo. 
![[Pasted image 20240329191523.png]]

● Una línea inicial de request (solicitud) tiene tres partes: 
* El nombre del método, en mayúsculas. 
* El path local del recurso solicitado.
* La versión de HTTP utilizada. 
* GET path/to/file/index.html HTTP/1.0
● Una línea inicial de response (respuesta) tiene tres partes:
- La versión HTTP. 
- El [[código de status de la respuesta]].
- Descripción del status. 
	- HTTP/1.0 200 OK 
	- HTTP/1.0 404 Not Found 
● El primer dígito del código de status identifica la categoría: 
- 1xx indica un mensaje de información únicamente. 
- 2xx indica éxito en general. 
- 3xx redirecciona el cliente a otro URL. 
- 4xx indica un error en la parte del cliente.
- 5xx indica un error en la parte del servidor.

[[HTTP]]
[[Servidores Web]]
[[Fundamentos de la WWW]]