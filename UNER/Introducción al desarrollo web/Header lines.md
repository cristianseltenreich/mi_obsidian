 ● Las líneas de encabezamiento proveen información sobre el pedido, la respuesta o el objeto que se está enviando en el cuerpo del mensaje. 
 ● La estructura es Header
 - Name:  value 
 - HTTP 1.0 define 46 headers pero ninguno es requerido.
 - HTTP 1.1 define 46 headers y requiere uno, el denominado Host, en los pedidos realizados. 
 ● Algunos headers importantes del cliente: 
 - User-agent: es el programa que realiza el pedido, de la forma "Nombre/x.xx" 
 - Ejemplo: User-agent: Chrome/44.0.2403.157 
 ● Algunos headers importantes del servidor: 
 - Server: identifica el software del servidor, en el mismo formato "Nombre/x.xx"
 - Ejemplo: Server: Apache/2.4.2 (Win32) 
 - Last modified: es la fecha de modificación del recurso otorgado.


[[HTTP]]
[[Request & Response]]
[[Servidores y Clientes]]
[[Modelo Cliente - Servidor]]
[[Métodos HTTP]]