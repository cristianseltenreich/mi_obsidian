- A través de diversos mecanismos, asegura que las transmisiones se lleven a cabo, en orden y sin errores.
- Primero los datos se dividen en paquetes con el formato establecido por el protocolo Transmission Control Protocol (TCP).
- Segundo, cada paquete es confirmado desde el receptor al emisor (tcp).
- En caso que se pierda un paquete el transmisor se va a dar cuenta que falta porque no hay un ACK (o confirmación) para ese paquete.
- El paquete es retransmitido, a pesar de estar fuera de orden y vuelto a ordenar en el destino.

![[Pasted image 20240324231235.png]]

[[Protocolos de Internet]]