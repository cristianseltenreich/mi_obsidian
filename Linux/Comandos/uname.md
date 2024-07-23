El siguiente comando muestra información sobre el sistema actual. Para poder ver el nombre del kernel que estás utilizando, introduce el siguiente comando en la terminal:

uname

El resultado debe ser similar al siguiente:
![[Pasted image 20240318194947.png]]

Muchos de los comandos que se ejecutan producen salida de texto como ésta. Puedes cambiar la salida producida con un comando mediante el uso de las opciones  después del nombre del comando.

Las opciones para un comando se pueden especificar de varias formas. Tradicionalmente, en UNIX, las opciones se expresaban por un guión seguido por otro carácter, por ejemplo: `-n`.

En Linux, las opciones pueden a veces también ser dadas por dos caracteres de guión seguidos por una palabra o palabra con guión, por ejemplo: `--nodename`.

Ejecuta el comando `uname` de nuevo dos veces en la terminal, una vez con la opción `-n` y de nuevo con la opción `--nodename`. Esto mostrará el nombre del host del nodo de la red, también visualizado en el prompt.

uname -n
uname --nodename

El resultado debe ser similar al siguiente:
![[Pasted image 20240318195403.png]]
![[Pasted image 20240318195604.png]]

[[Linux]]
[[La sintaxis de la Línea de Comandos]]