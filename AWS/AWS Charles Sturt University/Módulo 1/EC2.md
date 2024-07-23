- Definición: Un servicio que proporciona capacidad informática segura y redimensionable en la nube. Está diseñado para facilitar a los desarrolladores la computación en nube a escala web.
- Definición alternativa: EC2 es un servicio que permite alquilar máquinas virtuales que se ejecutan en los centros de datos de Amazon.
- La terminología de AWS para una máquina virtual es "instancia".
- El término industrial VPS es análogo a instancia

##### EC2 como máquina virtual

AWS indica: "Las instancias EC2 son efímeras". Pero esto no es un requisito. 

Las "instancias" pueden desempeñar el papel tradicional - reemplazar servidores on-premise/VPS/co-lo

EBS para almacenamiento de bloques
	- Una SAN virtual, de hasta 20.000 IOPS y 500 MB/s
	- Tolerancia a fallos
	
Recuperación de instancias
El tiempo de actividad y la vida útil de las máquinas son anecdóticamente "buenos".
Aprovisionamiento de autoservicio: importante para la disponibilidad

##### EC2 como debe utilizarse

- Sin SPOF  (single point of failure) -punto único de fallo-
- Escala horizontalmente, no verticalmente.
- Elástico
- Tratar las máquinas como desechables / diseño para fallos
	Chaos Monkey Netflix [GitHub - Netflix/chaosmonkey: Chaos Monkey is a resiliency tool that helps applications tolerate random instance failures.](https://github.com/Netflix/chaosmonkey)
- Tratar los centros de datos (zonas de disponibilidad) de la misma manera


[[Módulo 1 - Máquinas virtuales]]
[[Iniciar una máquina virtual Linux]]
