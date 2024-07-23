● No es suficiente conocer la ubicación del servidor. Ejemplo: IP + puerto. 
* Es necesario saber la forma de comunicación que debe seguirse: las reglas del diálogo, la estructura de los mensajes, etc. 
* Esto requiere una combinación de protocolos de bajo y alto nivel. 
● Algunos aspectos relacionados con el rol del servidor: 
* Autenticación. 
* Autorización.
* Seguridad de los datos.
* Privacidad. 
* Concurrencia. 
* Eficiencia.
[[Servidores y Clientes]]
[[Modelo Cliente - Servidor]]
[[HTTP]]
[[Fundamentos de la WWW]]

Las tecnologías que se encargan de trabajar del lado del servidor devolverán al cliente un resultado que pueda ser comprendido por el navegador. Algunos servidores Web (HTTP) son: 

**Apache HTTP Server Project**: proyecto colaborativo que tiene por finalidad el desarrollo de un servidor Web libre, robusto con capacidades de uso comercial. Tiene su origen en NCSA HTTPd desarrollado originalmente por Rob McCool. Puede ejecutar scripts de lenguajes como PHP, Perl, Python y Ruby. 
A un año de su salida se trataba del servidor Web más utilizado en el mundo.

**Nginx**: Es un servidor Web/proxy inverso, mail proxy y proxy TCP genérico programado originalmente por Igor Sysoev. Es software libre y de código abierto, licenciado bajo BSD simplificada. Es multiplataforma. 
El sistema es usado por una larga lista de sitios Web conocidos como: Yandex, VK, WordPress, Netflix, GitHub, SourceForge, TorrentReactor y partes de Facebook (como el servidor de descarga de archivos pesados).

**Internet Information Services (IIS)**: es un servidor Web y un conjunto de servicios para sistemas operativos Windows. Se encuentra integrado a los sistemas operativos para servidores Windows y las ediciones profesionales o superiores. Ofrece servicios como: FTP, SMTP, NNTP y HTTP/HTTPS. Ejecuta scripts en ASP, ASP.net, PHP y Perl. 

**Apache Tomcat**: es un servidor Web y un contenedor de servlets open source desarrollado por la ASF. Implementa varias especificaciones de Java EE entre los que se incluyen servlets, JSP, EL y Web Sockets.

**GlassFish/Payara**: es un proyecto de desarrollo de servidor de aplicaciones open source iniciado por Sun Microsystems para la plataforma JavaEE. Se trata de la implementación de referencia de JavaEE soportando: EJB, JPA, JSF, JMS, RMI, JSP y servlets.

**WEBrick**: servidor HTTP que permite ejecutar scripts Ruby.

**Node.JS**: si bien es un entorno de ejecución basado en el lenguaje de programación ECMAScript y por tanto, no se trata de un servidor Web se destaca la facilidad de crear uno utilizando el módulo http. 

	const http = require('http');
		//Crea el objeto servidor: 
	http.createServer(function (req, res) {
		res.write('Hello World!'); 
		//Escribe la respuesta al cliente.
		res.end();
		//Se cierra la respuesta. 
	}).listen(3000);
	//Indica que el servidor atiende en el puerto 3000