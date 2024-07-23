Matando Procesos

Le pedimos al proceso que finalice su ejecución (señal TERM). 

$ kill PID 

Si el proceso no obedece, le enviamos la señal KILL al Kernel para que lo finalice. 

$ kill -SIGKILL PID o $ kill -9 PID 

Para finalizar un proceso por su nombre: 

$ killall firefox Finaliza todos los procesos de firefox.

En este caso finalizo gedit con kill pid y luego muestro los procesos para ver que ya no está en ejecución
![[Pasted image 20240429201119.png]]


