
1. **Hashing de contraseñas y su conversión:** Cuando un usuario elige una contraseña, esta se convierte en un hash mediante una función criptográfica como MD5 o SHA. En teoría, nadie, ni siquiera el administrador del sistema, debería poder recuperar el texto sin formato a partir del hash. Sin embargo, los ataques de texto plano sin cifrar pueden explotar el almacenamiento de contraseñas o protocolos de autenticación de red que no utilizan cifrado. Ejemplos de estos protocolos incluyen PAP, autenticación básica, HTTP, FTP y Telnet, que no deben utilizarse.
    
2. **Ataques de contraseñas en línea:**
    
    - En un ataque de contraseña en línea, el atacante interactúa directamente con el servicio de autenticación, como un formulario de inicio de sesión web o una puerta de enlace VPN. Envía contraseñas utilizando una base de datos conocida o una lista de contraseñas previamente descifradas sin conexión.
    - Existen bases de datos de combinaciones de hash de nombre de usuario y contraseña almacenadas en Internet, derivadas de hacks exitosos en sistemas de diversas empresas.
    - Los informes de auditoría pueden mostrar inicios de sesión fallidos repetidos seguidos de un inicio de sesión exitoso o intentos de inicio de sesión en momentos o ubicaciones inusuales.
3. **Mitigación de ataques de contraseñas en línea:**
    
    - Restringir el número o la tasa de intentos de inicio de sesión y evitar intentos desde direcciones IP incorrectas conocidas.
    - Sin embargo, restringir los inicios de sesión puede exponer la cuenta a ataques de denegación de servicio, ya que el atacante continuará intentando autenticarse bloqueando a los usuarios válidos.
4. **Ataque en línea horizontal de fuerza bruta:**
    
    - En este tipo de ataque, el atacante prueba una o más contraseñas comunes (por ejemplo: 1, 2, 3, 4, 5, 6) junto con varios nombres de usuario.
    - En contraste, un ataque fuera de línea implica obtener una base de datos de hashes de contraseñas (como SystemRoot, System32 o etc/shadow). El atacante no interactúa con el sistema de autenticación, y el registro de auditoría del sistema de archivos registra la cuenta maliciosa que accede a uno de estos archivos.
5. **Ataques de contraseñas mediante rastreo de paquetes:**
    
    - Si el atacante no puede obtener una base de datos de contraseñas, puede utilizar un rastreador de paquetes para obtener la respuesta del cliente a un desafío del servidor en protocolos como NTLM o CHAP y MS-CHAP.
    - Estos protocolos evitan enviar directamente el hash de la contraseña, pero los crackers de contraseñas pueden aprovechar debilidades para calcular el hash y hacerlo coincidir con una palabra del diccionario o mediante fuerza bruta.

[[Operaciones y respuesta a incidentes de ciberseguridad (CompTIA Security+ SY0-601]]
