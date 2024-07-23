
Muchos usuarios utilizamos  linux dentro de una máquina virtual en VirtualBox y tenemos la necesidad de compartir contenido entre la máquina anfitriona y la huesped. 

Vamos a ver entonces cómo cómo montar en una máquina virtual con Ubuntu (huesped) una carpeta compartida de Windows (la anfitriona) en VirtualBox.


Vamos a agregar la carpeta compartida con la máquina virtual en marcha.

Para ello previamente creamos una carpeta en la anfitriona, en mi caso creo la carpeta bodhilinux en el escritorio de Windows.

Paso seguido creamos una carpeta en la máquina virtual huésped. En mi caso creo la carpeta windows en el escritorio de mi Ubuntu corriendo en Virtual Box.

![[Pasted image 20240617105350.png]]


Luego, teniendo seleccionada mi máquina virtual, desde la configuración de la misma en Virtual Box, accedemos desde el menú `Configuración > Carpetas compartidas`. 
![[Pasted image 20240617105615.png]]

Presiono el símbolo + y se abre un formulario donde vamos a indicar:
 * la ruta completa de la carpeta creada en la anfitriona
 * el nombre de la carpeta creada en la anfitriona.
 * el punto de montaje, que es la ruta completa de la carpeta creada en la máquina virtual Ubuntu
 * Seleccionamos Automontar y Hacer permanente

![[Pasted image 20240617105259.png]]


Una vez hecho esto, nos vamos a la máquina virtual y abrimos una terminal  y montamos la carpeta compartida con el siguiente comando:

sudo mount -t vboxsf nombre_carpeta_anfitriona /ruta/carpeta_maquina_virtual

![[Pasted image 20240617105852.png]]

Y voila, a partir de 
ese momento quedará montada esa carpeta compartida de manera bidireccional.