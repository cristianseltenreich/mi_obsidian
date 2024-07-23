$ ps 
Muestra un listado con los procesos del sistema 
![[Pasted image 20240425113436.png]]

$ ps -aux 
-a muestra los procesos de todos los usuarios
-x muestra los procesos de todas las terminales 
-u muestra la información en forma más amigable

![[Pasted image 20240425113659.png]]
que significa cada encabezado para entender los datos:
![[Pasted image 20240425113806.png]]


Para averiguar información específica de un proceso. 

$ ps -ax | grep comando

![[Pasted image 20240425175654.png]]


Averiguar el PID de un proceso 

$ pgrep nombre_interno 

![[Pasted image 20240425180118.png]]


$ pgrep -f comando

![[Pasted image 20240425180252.png]]


