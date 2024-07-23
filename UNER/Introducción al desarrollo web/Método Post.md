El método POST es esencial para la interacción Web. 
- Este método envía información al servidor para ser procesada por quien corresponda, como un script CGI, PHP, Node JS, Java o cualquier tecnología del lado del servidor. 
● Diferencias con el GET:
- Se envía un bloque de datos adicional, en forma de headers. 
- El URI no es un recurso a transferir, sino el responsable del procesamiento.
- El resultado a transferir es el output de ese procesamiento. 
● El método POST se utiliza típicamente para enviar información desde un formulario. 
● Sin embargo, el método GET también puede utilizarse para el mismo fin! 
- Esto es así dado que los datos pueden incluirse en el URL 
- Solo debe utilizarse cuando los datos son reducidos. 
- Caso contrario, deberá utilizarse el método POST.
● En ambos casos, el URL será codificado (URL-encoded) para transmitir los caracteres especiales (espacio, &, %, etc.) 
● Al momento de implementar un cliente o un servidor Web deben tenerse en cuenta estos y muchos otros detalles para entablar una conversación HTTP.

[[Métodos HTTP]]
[[Solicitudes GET y POST]]