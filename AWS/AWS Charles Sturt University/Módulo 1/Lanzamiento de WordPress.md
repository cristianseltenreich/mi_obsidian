[https://aws.amazon.com/getting-started/tutorials/launch-a-wordpress-website/?trk=gs_card](https://aws.amazon.com/getting-started/tutorials/launch-a-wordpress-website/?trk=gs_card)

##### Información general

[Amazon Lightsail](https://aws.amazon.com/lightsail/?p=gsrc&c=ho_lww) es una de las formas más fáciles de comenzar a utilizar AWS. Ofrece servidores virtuales, almacenamiento, bases de datos y redes, además de un plan mensual rentable.

Este tutorial muestra cómo lanzar y configurar una instancia de WordPress en Lightsail. Incluye pasos para conectarse a la instancia mediante SSH, iniciar sesión en el sitio web de WordPress, crear una IP estática y asociarla a la instancia, crear una zona DNS y asignarla a la instancia. 

Al finalizar este tutorial, conocerá los aspectos fundamentales para poner en funcionamiento su sitio web de WordPress en Amazon Lightsail.


##### Paso 1: creá una cuenta de Amazon Lightsail

Este tutorial se puede hacer en el nivel gratuito de AWS.
[Comenzá a utilizar Lightsail gratis!.](https://portal.aws.amazon.com/billing/signup?client=lightsail&fid=1A3F6B376ECAC516-2C15C39C5ACECACB&redirect_url=https%3A%2F%2Flightsail.aws.amazon.com%2Fls%2Fsignup#/start)

![[Pasted image 20240310151553.png]]
##### Paso 2: cree una instancia de WordPress en Lightsail

Completá los siguientes pasos para poner su instancia de WordPress en funcionamiento en Lightsail.

**Nota:** Para más información sobre cómo crear una instancia en Lightsail, podés consultar como [crear una instancia de Amazon Lightsail](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/how-to-create-amazon-lightsail-instance-virtual-private-server-vps) en la documentación de Lightsail. 

a. Iniciá sesión en la [consola de Lightsail](https://lightsail.aws.amazon.com/). 

b. En la pestaña Instancias de la página de inicio de Lightsail, elija **Crear instancia**.

![[Pasted image 20240310151500.png]]
c. La región y la zona de disponibilidad de AWS se seleccionan. Elija **Change AWS Region and Availability Zone** (Cambiar la región y la zona de disponibilidad de AWS) si quiere crear la instancia en otra ubicación.

![[Pasted image 20240310151724.png]]
![[Pasted image 20240310151758.png]]

d. Elija su imagen de instancia.

- Elija **Linux/Unix** como plataforma.
- Elija **WordPress** como modelo.
![[Pasted image 20240310151904.png]]

e. Elija un plan de instancia.

Un plan incluye la configuración de una máquina (RAM, SSD, CPU virtual) a un costo bajo y predecible, y la transferencia de datos permitida. Puede probar el plan de 3,50 USD de Lightsail sin cargo durante un tres meses (hasta 750 horas). AWS bonifica los tres primeros meses en su cuenta.

![[Pasted image 20240310152026.png]]

f. Ingrese un nombre para la instancia y elija **Create instance** (Crear instancia).

Directrices de nombre de recurso:

- Debe ser único dentro de cada región de AWS en su cuenta Lightsail.
- Debe contener de 2 a 255 caracteres.
- Debe comenzar y finalizar con un carácter o número alfanumérico.
- Puede incluir caracteres alfanuméricos, números, puntos, guiones y guiones bajos.

![[Pasted image 20240310152254.png]]

![[Pasted image 20240310152427.png]]
Recargar para confirmar que está corriendo (running)

##### Paso 3: conéctese a la instancia a través de SSH y obtenga la contraseña para el sitio web de WordPress

La contraseña predeterminada para iniciar sesión en el panel de administración del sitio web de WordPress se almacena en la instancia.

Complete los siguientes pasos para conectarse a la instancia mediante el cliente SSH basado en navegador en la consola de Lightsail y obtenga la contraseña para el panel de administración.

**Nota:** Para más información, consulte [Obtención del nombre de usuario y la contraseña de aplicación para la instancia de Bitnami en Amazon Lightsail](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/log-in-to-your-bitnami-application-running-on-amazon-lightsail).

a. En la pestaña **Instancias** de la [página de inicio de Lightsail](https://lightsail.aws.amazon.com/), elija el icono de conexión rápida de SSH para su instancia de WordPress.

![[Pasted image 20240310153957.png]]

![[Pasted image 20240310153054.png]]

b. Después de que se abra la ventana del cliente SSH basado en el navegador, ingrese el siguiente comando para recuperar la contraseña predeterminada de la aplicación:

```plainText
cat $HOME/bitnami_application_password
```


##### Paso 4: inicie sesión en el panel de administración del sitio web de WordPress

Ahora que tiene la contraseña para el panel de administración del sitio web de WordPress, puede iniciar sesión. En el panel de administración, puede cambiar su contraseña de usuario, instalar complementos, cambiar el tema de su sitio web y más.

Complete los siguientes pasos para iniciar sesión en el panel de administración del sitio web de WordPress.

**Nota**: Para más información, consulte [Obtención del nombre de usuario y la contraseña de aplicación para la instancia de Bitnami en Amazon Lightsail](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/log-in-to-your-bitnami-application-running-on-amazon-lightsail).

a. En un navegador, vaya a:

```plainText
http://PublicIpAddress/wp-login.php
```
En la dirección, reemplace **PublicIpAddress** por la dirección IP pública de la instancia de WordPress. Puede obtener la dirección IP pública de la instancia en la consola de Lightsail como se muestra en la imagen a la derecha:
![[Pasted image 20240310154050.png]]

b. Inicie sesión en la instancia. 

- En la casilla **Username** (Nombre de usuario) o **Email address** (Dirección de correo electrónico), ingrese _user_ (usuario).
- En el cuadro **Password** (Contraseña), ingrese la contraseña predeterminada obtenida anteriormente en este tutorial.  
    
- Elija **Log in** (Iniciar sesión).
![[Pasted image 20240310154152.png]]

![[Pasted image 20240310154352.png]]

##### Paso 5: cree una dirección IP estática de Lightsail y asóciela a la instancia de WordPress

La IP pública predeterminada para la instancia de WordPress cambia si detiene e inicia la instancia. Una dirección IP estática, asociada a una instancia, permanece igual incluso si detiene e inicia su instancia.

Complete los siguientes pasos para crear una dirección IP estática y asociarla a la instancia de WordPress.

**Nota:** Para obtener más información, consulte [Crear una IP estática y asociarla a una instancia en Amazon Lightsail.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/lightsail-create-static-ip)  

a. En la pestaña **Instancias** de la página de [inicio de Lightsail](https://lightsail.aws.amazon.com/), elija su instancia de WordPress en ejecución.
![[Pasted image 20240310154832.png]]

![[Pasted image 20240310155026.png]]
![[Pasted image 20240310155347.png]]
d. Asigne un nombre a la IP estática y, luego, elija **Create** (Crear).
![[Pasted image 20240310155523.png]]
![[Pasted image 20240310155629.png]]

##### Paso 6: asigne un dominio a la instancia de WordPress

Esto le permite asignar más fácilmente un dominio a la instancia de WordPress y administrar más recursos del sitio web mediante la consola Lightsail.


**Nota:** Para obtener más información, consulte [Creación de una zona DNS para administrar los registros DNS de su dominio en Amazon Lightsail.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/lightsail-how-to-create-dns-entry)

a. En la pestaña **Domains** de la página de [inicio de Lightsail](https://lightsail.aws.amazon.com/), elija **Crear zona DNS**.


![[Pasted image 20240310160524.png]]
No voy a registrar el dominio porque tiene un costo de U$d 13. Pero simplemente hay que seguir los pasos:

![[Pasted image 20240310160746.png]]
##### Paso 7: eliminar instancia

a. En la pestaña **Instances** (Instancias) de la [página de inicio de Lightsail](https://lightsail.aws.amazon.com/), elija el icono de elipsis vertical (⋮) situado junto a la instancia de WordPress que acaba de crear y elija **Delete** (Eliminar).

![[Pasted image 20240310160940.png]]

![[Pasted image 20240310161012.png]]

## Conclusión

Utilizamos Amazon Lightsail para lanzar e implementar una instancia de WordPress.  

Amazon Lightsail es una excelente opción para desarrollar, crear e implementar una variedad de aplicaciones como WordPress, sitios web y plataformas de blogs.  

