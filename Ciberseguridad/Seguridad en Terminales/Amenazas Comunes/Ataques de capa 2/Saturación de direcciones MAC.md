![[Pasted image 20240208123211.png]]

Los dispositivos en una red se conectan a través de un switch de red mediante la conmutación de paquetes para recibir y reenviar datos al dispositivo de destino.

La inundación de MAC compromete los datos transmitidos a un dispositivo.

Un atacante inunda la red con direcciones MAC falsas, comprometiendo la seguridad del switch de red. Esta condición ahora permite que un atacante capture todas las tramas enviadas desde un host a otro en la LAN local o VLAN local.

[Una herramienta como macof puede saturar un switch con hasta 8,000 tramas falsas por segundo, creando un ataque de saturación de la tabla de direcciones MAC en cuestión de segundos](https://ccnadesdecero.es/ataque-tabla-direcciones-mac/)

Para mitigar los ataques de saturación de la tabla de direcciones MAC, los administradores de red deben implementar la seguridad del puerto. Seguridad de puertos (Port security) permitirá que el puerto aprenda sólo un número específico de direcciones MAC de origen. Seguridad de puertos (Port security).

Tags
[[Ataques Cibernéticos]]
[[Ataques de capa 2]]
