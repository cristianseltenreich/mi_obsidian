fuente [Cómo ver hilos de un proceso en Linux (linux-console.net)](https://es.linux-console.net/?p=8962#:~:text=El%20comando%20top%20puede%20mostrar%20una%20vista%20en,ejecuta%20top%2C%20presionando%20la%20tecla.%20%24%20top%20-H)

> **Pregunta:** Mi programa crea y ejecuta varios subprocesos en él. ¿Cómo puedo monitorear subprocesos individuales del programa una vez que se crean? Me gustaría ver los detalles (por ejemplo, uso de CPU/memoria) de subprocesos individuales con sus nombres.

Los subprocesos son una abstracción de programación popular para la ejecución paralela en los sistemas operativos modernos. Cuando los subprocesos se bifurcan dentro de un programa para múltiples flujos de ejecución, estos subprocesos comparten ciertos recursos (por ejemplo, espacio de direcciones de memoria, archivos abiertos) entre ellos para minimizar la sobrecarga de bifurcación y evitar el costoso canal IPC (comunicación entre procesos). Estas propiedades hacen que los subprocesos sean un mecanismo eficiente para la ejecución simultánea.

En Linux, los subprocesos (también llamados procesos ligeros (LWP)) creados dentro de un programa tendrán el mismo "ID de grupo de subprocesos" que el PID del programa. Cada subproceso tendrá entonces su propio ID de subproceso (TID). Para el programador del kernel de Linux, los hilos no son más que procesos estándar que comparten ciertos recursos. Las herramientas clásicas de línea de comandos como `ps` o `top`, que muestran información a nivel de proceso de forma predeterminada, pueden recibir instrucciones para mostrar subprocesos información de nivel.

## Cómo ver hilos de un proceso en Linux
---

Aquí hay varias formas de **mostrar subprocesos para un proceso en Linux**. Si simplemente desea contar la cantidad de hilos en un hilo, consulte esta publicación en su lugar.

busco un procesos con ps por ejemplo y elijo el que quiero ver sus hilos o threads, en este caso por ejemplo el PID gedit

![[Pasted image 20240429193753.png]]


**averiguar los hilos con ps**
$ ps -T -p |pid|
![[Pasted image 20240429194457.png]]

**averigurar los hilos con top**
$ top -H -p |pid| para mostrar los hilos de un proceso

![[Pasted image 20240429193517.png]]
