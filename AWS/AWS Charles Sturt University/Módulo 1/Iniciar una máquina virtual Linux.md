
##### Tutorial Amazon para iniciar una máquina virtual
[https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/?trk=gs_card](https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/?trk=gs_card)


##### Paso 1: cree una cuenta de Amazon Lightsail

![[Pasted image 20240309114400.png]]
##### Paso 2: cree una instancia de Amazon Linux en Lightsail

![[Pasted image 20240309114445.png]]
##### Paso 3: configure su instancia de Amazon Lightsail

a. La región y la zona de disponibilidad de AWS se seleccionan. **Elija Cambiar región y Zona de disponibilidad** para crear su instancia en otra ubicación. _Nota: Las direcciones IP estáticas solo se pueden adjuntar a instancias de la misma región._
![[Pasted image 20240309114537.png]]

![[Pasted image 20240309114744.png]]
![[Pasted image 20240309114826.png]]

b. Elija la opción de la plataforma **Linux/Unix** y **Solo SO** para ver las imágenes de instancias del sistema operativo solamente que se encuentran disponibles en Lightsail.

Para obtener más información sobre las imágenes de instancias de Lightsail, consulte [Elegir una imagen de instancia de Amazon Lightsail.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/compare-options-choose-lightsail-instance-image)

c. Elija la opción de esquema de **Amazon Linux 2**.

![[Pasted image 20240309115047.png]]

d. (Opcional) Elija **Agregar script de lanzamiento** para agregar un script shell que se ejecutará en la instancia cuando se lance.

![[Pasted image 20240309115523.png]]
e. (Opcional) Elija **Cambiar el **par** de claves de SSH** para seleccionar, crear o cargar el par de claves que desea usar para establecer una conexión SSH con su instancia.
![[Pasted image 20240309115617.png]]

f. (Opcional) Elija **Enable Automatic Snapshots** (Habilitar las instantáneas automáticas) para crear automáticamente y a diario una imagen que funcione como copia de seguridad de su instancia y los discos asociados.

![[Pasted image 20240309115744.png]]

g. Elija el plan de la instancia. Puede probar el plan de 3,50 USD de Lightsail sin cargo durante los tres primeros meses (hasta 750 horas). Bonificaremos los tres primeros meses en su cuenta.

Obtenga más información en la [página de precios de Lightsail](https://aws.amazon.com/lightsail/pricing/?p=gsrc&c=ho_lvm).
![[Pasted image 20240309115853.png]]

h. Escriba un nombre para la instancia.
![[Pasted image 20240309120031.png]]
i. (Opcional) Elija una de las siguientes opciones para agregar etiquetas a la instancia:

- (Opcional) Agregar etiquetas de solo clave: ingrese la nueva etiqueta en el cuadro de texto correspondiente a la clave de la etiqueta y pulse **Intro**. Elija **Guardar** cuando termine de escribir las etiquetas para agregarlas o **Cancelar** para no agregarlas.
- (Opcional) Crear una etiqueta de clave-valor: escriba una clave en el cuadro de texto **Clave** y un valor en el cuadro de texto **Valor**. Elija **Guardar** cuando termine de escribir las etiquetas o **Cancelar** para no agregarlas.

Las etiquetas de clave-valor solo se pueden agregar de a una antes de guardarlas. Para agregar más de una etiqueta de clave-valor, repita los pasos anteriores.  
  
Si desea obtener más información sobre las etiquetas de solo clave y de clave-valor, consulte [Etiquetas en Amazon Lightsail.](https://lightsail.aws.amazon.com/ls/docs/en_us/articles/amazon-lightsail-tags)

![[Pasted image 20240309120253.png]]
j. Elija **Crear instancia.**
![[Pasted image 20240309120324.png]]

Instancia creada, nótese que está "pendiente" inicialmente

![[Pasted image 20240309120436.png]]

![[Pasted image 20240309120541.png]]

Al recargar el navegador la instancia está creada
![[Pasted image 20240309120912.png]]
##### Paso 4: conéctese a la instancia.

Conéctese a la instancia usando el terminal SSH basado en el navegador en Lightsail.

a. En la pestaña **Instancias** de la página principal de Lightsail, elija el icono de terminal o el icono de elipsis (⋮) junto a la instancia de Amazon Linux que acaba de crear.

Aparece la ventana del terminal SSH basado en el navegador. Puede escribir los comandos de Linux en el terminal del navegador y administrar su instancia sin configurar un cliente de SSH.

![[Pasted image 20240309121004.png]]

![[Pasted image 20240309121207.png]]

Creo el archivo prueba.txt y lo visualizo en la instancia creada

![[Pasted image 20240309121516.png]]

##### Detener la instancia

Importante! Al finalizar la prueba, no olvidar detener la instancia para que no genere costos! 
![[Pasted image 20240309121952.png]]
![[Pasted image 20240309122121.png]]

![[Pasted image 20240309122205.png]]
Asegurarse que haya quedado apagada la instancia
![[Pasted image 20240309122334.png]]

##### Conclusión

Utilizamos Amazon Lightsail para poner en funcionamiento y configurar fácilmente una instancia de Linux.  
  
Amazon Lightsail es ideal para desarrolladores, profesionales web y cualquier persona que quiera comenzar a utilizar AWS de manera rápida y económica. Puede lanzar instancias, bases de datos y almacenamiento en SSD, transferir datos, supervisar sus recursos y mucho más de manera administrada.    
  
Independientemente de que sea un solo desarrollador que crea un proyecto o un bloguero que crea un sitio web personal, Amazon Lightsail es una muy buena manera para comenzar.  



tags
[[Instances]]