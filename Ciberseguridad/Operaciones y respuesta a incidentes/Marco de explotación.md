1. **Troyanos de acceso remoto (RAT) y su propósito:** Los troyanos de acceso remoto (RAT) son tipos de malware que permiten a un adversario acceder de forma remota a una red o sistema. Desde la perspectiva de la evaluación de la postura de seguridad, un probador de penetración podría querer establecer una conexión RAT para intentar enviar información corporativa a través de canales de exfiltración de datos. Sin embargo, cuando los controles de seguridad funcionan correctamente, estos intentos deben ser detectados o rechazados.
    
2. **Marcos de explotación y su enfoque:** Un marco de explotación utiliza vulnerabilidades identificadas por escáneres automatizados y lanza scripts o software para entregar exploits coincidentes. Esto puede causar interrupciones significativas en el objetivo, incluyendo fallas en el servicio y riesgos para la seguridad de los datos.
    
3. **Componentes de un marco de explotación:**
    
    - **Base de datos de códigos de explotación:** Contiene exploits dirigidos a vulnerabilidades y exposiciones comunes (CVE).
    - **Cargas útiles modulares:** El código de explotación se combina con estas cargas útiles. Dependiendo del acceso obtenido, las cargas útiles pueden abrir un Shell de comandos, crear usuarios, instalar software, etc.
    - **Módulos de explotación personalizados:** Pueden inyectarse en el sistema de destino.
    - **Ofuscación del código:** Permite que el código se inyecte más allá de sistemas de detección de intrusos o software antivirus.
4. **Metasploit: El marco de exploits más conocido:** Metasploit es un software de código abierto mantenido por Rapid7. Ofrece una edición comunitaria con paquetes de instalación para Linux y Windows. Rapid7 también produce ediciones comerciales Pro y Express del marco, que se integran estrechamente con el escáner de vulnerabilidades Nexpose.
    
5. **Marco Sn1per para pruebas de penetración:** El marco Sn1per está diseñado para informes de recopilación y pruebas de penetración. Puede integrarse con otras herramientas como Metasploit y Nikto para ejecutar conjuntos de pruebas automatizados, y los resultados se pueden mostrar como informes web.

[[Operaciones y respuesta a incidentes de ciberseguridad (CompTIA Security+ SY0-601]]