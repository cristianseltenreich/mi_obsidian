
ARP son las siglas de Address Resolution Protocol, que en español se traduce como Protocolo de Resolución de Direcciones1. Es un protocolo de comunicaciones de la capa de enlace de datos que se encarga de encontrar la dirección de hardware (Ethernet MAC) que corresponde a una determinada dirección IP.

El protocolo ARP permite a un dispositivo conectado a una red LAN obtener la dirección MAC de otro dispositivo conectado a la misma red LAN cuya dirección IP es conocida1. Para ello, se envía un paquete (ARP request) a la dirección de difusión de la red (broadcast, MAC = FF:FF:FF:FF:FF:FF) que contiene la dirección IP por la que se pregunta, y se espera a que esa máquina (u otra) responda (ARP reply) con la dirección Ethernet que le corresponde.

Cada máquina mantiene una caché con las direcciones traducidas para reducir el retardo y la carga. Las entradas de la tabla se borran cada cierto tiempo, ya que las direcciones físicas de la red pueden cambiar.

Es importante mencionar que el protocolo ARP es fundamental para el buen funcionamiento de las redes, ya que facilita el reconocimiento de los dispositivos y la comunicación entre ellos