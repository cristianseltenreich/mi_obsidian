- Instancias de AWS.
- Diferentes tipos de instancias
- Precios
- Diferencias entre AWS EC2 y otras soluciones, incluidas las locales, y VPS
- Programación para aprovechar la potencia de AWS EC2

##### Visión general

Este módulo se centra en lo que podría considerarse la piedra angular de los servicios de Amazon: EC2. [[EC2]] son las siglas de Elastic Compute Cloud. EC2 le permite crear máquinas virtuales con acceso predeterminado a través de RDP (Windows) o SSH (Linux).

La experiencia no es diferente a la ejecución de máquinas virtuales en su propia máquina o servidores, excepto que toda la infraestructura subyacente se administra automáticamente y se incorpora en el precio por hora. No se debe subestimar el valor de que otra persona compre y administre todo esto por usted: hardware de servidor/red/rack, refrigeración, energía, instalaciones, personal, etc. Gran parte del atractivo de servicios como EC2 es la suposición de que todo el mundo se beneficia de la eficiencia de escala.

Pero lo que EC2 (y cualquier otro servicio de computación **en la nube** de la competencia) hace, además de proporcionar máquinas virtuales, es proporcionar a los clientes la capacidad de agregar o eliminar automáticamente servidores ("instancias", en la jerga de EC2) según sea necesario. Esto se puede hacer mediante programación mediante la API o los SDK de AWS o, más comúnmente, mediante herramientas integradas, como los grupos de escalado automático de EC2. AWS, bajo el paraguas de "EC2", también contiene servicios como balanceadores de carga que se pueden configurar mediante la consola web (GUI) para que el tráfico se distribuya uniformemente entre sus servidores virtuales. El propósito de todo esto es lograr el santo grial de los servicios informáticos: computación elástica y de alta disponibilidad, donde solo pagas por lo que necesitas en un momento dado del año.

Exploraremos el funcionamiento real de EC2 en las lecturas de esta semana, la clase en línea y los deberes (laboratorios).

***
##### Video Youtube módulo 1
- https://youtu.be/vXDYiy-egCY?si=9h7MZqXL_4UkE5yS
##### Diapositivas módulo 1
- https://drive.google.com/file/d/11QwSsXBQ-Lfq6LCH2bYJhVmQL8T734rQ/view?usp=drive_link
***

##### Lecturas

###### Libro de texto:

- Kindle eBook: introducción a AWS Kindle Edition. Se puede leer en un navegador web. [https://awsdocs.s3.amazonaws.com/gettingstarted/latest/awsgsg-intro.pdf](https://awsdocs.s3.amazonaws.com/gettingstarted/latest/awsgsg-intro.pdf)  
    Información general de AWS - Regiones y zonas  
    de disponibilidad - Seguridad  
    - Servicios informáticos y de redes  
    
- Páginas de productos de EC2: [https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/)  
    
- Vale la pena leer las páginas de productos de cada servicio de AWS con el que entre en contacto. La página de inicio puede ser un poco vergonzosa de marketing, pero las otras páginas tienen mucha información importante. Especialmente las páginas de preguntas frecuentes y precios, donde AWS expone los datos fríos y concretos.
- https://aws.amazon.com/ec2/instance-types/
- Información sobre la capa gratuita de AWS: [https://aws.amazon.com/free/](https://aws.amazon.com/free/)
- Gran parte del uso de AWS es gratuito hasta cierto punto, obviamente para fomentar la adopción. Pero puedes hacer un cálculo bastante significativo antes de que te cobren nada.
- Pruebas independientes de la latencia de AWS entre zonas de disponibilidad: [https://www.quora.com/What-are-typical-ping-times-between-different-EC2-availability-zones-within-the-same-region](https://www.quora.com/What-are-typical-ping-times-between-different-EC2-availability-zones-within-the-same-region)

  

##### Actividades a realizar

- Regístrese para obtener su propia cuenta de AWS si aún no lo ha hecho
- Laboratorios semana 1
- Más información sobre las subredes IPv4.

***
#### Laboratorios

**[[Iniciar una máquina virtual Linux]]**
**[[Iniciar una máquina virtual de Windows]]**
**[[Lanzamiento de WordPress]]**


