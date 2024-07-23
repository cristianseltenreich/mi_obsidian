## Módulo 4 - Atacando lo que hacemos

4.0.1 ¿Por qué debería tomar este módulo?

Los fundamentos de la red deben estar protegidos, pero no es suficiente para proteger completamente nuestra red. Los protocolos que se utilizan para llevar a cabo las actividades diarias de la organización, también deben estar protegidos. Además, los protocolos y el software que proporcionan servicios a través de la red también pueden ser el objetivo de los atacantes. Un analista de ciberseguridad debe estar familiarizado con las vulnerabilidades y amenazas a los fundamentos de la comunicación de red.

En este módulo, aprenderá cómo funcionan los protocolos comúnmente utilizados en la empresa y cómo son vulnerables a ataques y explotaciones.

4.0.2 ¿Qué aprenderé en este módulo?

![[Pasted image 20240526203013.png]]

4.1 Servicios IP

4.1.1 Vulnerabilidades de ARP

Los hosts transmiten una solicitud ARP hacia otros hosts del segmento de red para determinar la dirección MAC de un host con una dirección IP específica. Todos los hosts de la subred reciben y procesan la solicitud de ARP. El host con la dirección IP que coincide con la de la solicitud de ARP envía una respuesta de ARP.

![[Pasted image 20240526203218.png]]

Cualquier cliente puede enviar una respuesta de ARP no solicitada llamada “ARP gratuito”. Esto suele hacerse cuando un dispositivo se inicia por primera vez para informar a todos los demás dispositivos de la red local sobre la nueva dirección MAC del dispositivo. Cuando un host envía un ARP gratuito, otros hosts en la subred almacenan en sus tablas de ARP la dirección MAC y la dirección IP que contiene dicho ARP.

Sin embargo, esta característica de ARP también significa que cualquier host puede afirmar ser el dueño de cualquier IP/MAC que elija. Un atacante puede envenenar la caché ARP de los dispositivos en la red local y crear un ataque MiTM para redireccionar el tráfico. El objetivo es asociar la dirección MAC del atacante con la dirección IP de la Puerta de enlace por defecto en las caché ARP de los hosts del segmento LAN. Esto posiciona al atacante entre la víctima y todos los demás sistemas fuera de la subred local.

4.1.2 Envenenamiento de caché de ARP

El envenenamiento de caché ARP se puede usar para lanzar varios ataques Man-in-the-middle.

Explicación del proceso de envenenamiento de caché ARP

**Solicitud Arp**
La figura muestra cómo funciona el envenenamiento de caché ARP. La PC-A requiere la dirección MAC de su Puerta de enlace por defecto (R1); por lo tanto, envía una solicitud ARP para la dirección MAC de 192.168.10.1.

![[Pasted image 20240526203446.png]]


**Respuesta Arp**
En está figura, R1 actualiza su caché ARP con las direcciones IP y MAC de la PC-A y envía una respuesta de ARP a PC-A, la cual a su vez, actualiza su caché ARP con las direcciones IP y MAC del R1.

![[Pasted image 20240526203615.png]]
**Respuestas Arp gratuitas falsificadas**
En la figura 3, el atacante envía dos respuestas de ARP gratuitas falsas usando su propia dirección MAC para las direcciones IP de destino indicadas. La PC-A actualiza su caché ARP con su Puerta de enlace por defecto, la cual ahora apunta hacia la MAC del host del atacante. El R1 también actualiza su caché ARP con la dirección IP de la PC-A y comienza a apuntar a la dirección MAC del atacante.

El anfitrión del atacante está ejecutando un ataque de envenenamiento ARP. El envenenamiento ARP puede ser pasivo o activo: Pasivo: Los atacantes roban información confidencial. Activo: Los atacantes modifican datos en tránsito o inyectan datos maliciosos.


![[Pasted image 20240526203756.png]]

**Nota:** Hay muchas herramientas disponibles en Internet para crear ataques de MITM de ARP, como dsniff, Cain & Abel, ettercap y Yersinia.

---

