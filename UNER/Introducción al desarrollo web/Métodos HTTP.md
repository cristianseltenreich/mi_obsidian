Además de GET, HTTP define los siguientes métodos: 
- HEAD: solicita una respuesta idéntica a la que correspondería a una petición GET, pero sin el cuerpo de la respuesta. 
- POST: Envía los datos para que sean procesados por el recurso identificado. Los datos se incluirán en el cuerpo de la petición. Esto puede resultar en la creación de un nuevo recurso o de las actualizaciones de los recursos existentes o ambas cosas. 
- PUT: realiza un upload de un recurso especificado (archivo). Es la alternativa más eficiente para subir archivos a un servidor, esto es porque en POST utiliza un mensaje multiparte y el mensaje es decodificado por el servidor. 
- PATCH: Sirve para aplicarle modificaciones parciales a un recurso. – DELETE: Borra el recurso especificado. 
- TRACE: solicita al servidor que envíe de vuelta en un mensaje de respuesta, en la sección del cuerpo de entidad, toda la información que reciba del mensaje de solicitud. Se utiliza con fines de comprobación y diagnóstico. 
- OPTIONS: Devuelve los métodos HTTP que el servidor soporta para un URL específico. Esto puede ser utilizado para comprobar la funcionalidad de un servidor Web mediante petición en lugar de un recurso específico. 
- CONNECT: Se utiliza para saber si se tiene acceso a un host.

[[Request & Response]]
[[HTTP]]
[[Método Post]]
