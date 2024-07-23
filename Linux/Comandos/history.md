El shell bash mantiene un historial de los comandos que introduces. Los comandos anteriores son fácilmente accesibles en esta historia de varias maneras.

La primera y más fácil manera de llamar o recordar un comando anterior es el uso de la **tecla de flecha arriba**. Cada presión de la **tecla de flecha arriba** va hacia atrás un comando a través del historial. Si accidentalmente vas atrás demasiado, entonces la tecla de flecha abajo irá hacia delante a través del historial de los comandos.

Cuando encuentres el comando que quieres ejecutar, puedes utilizar las t**eclas de flecha hacia izquierda** y **flecha hacia derecha** para colocar el cursor para edición. Otras teclas útiles para edición incluyen  **Inicio**, **Fin**, **Retroceso** y **Suprimir**.

#### history
Otra forma de utilizar el historial de comandos es ejecutar el comando `history` para poder ver una lista  numerada  del historial. El número que aparece a la izquierda del comando se puede utilizar para ejecutar el comando de nuevo. El comando `history` también tiene una serie de opciones y argumentos que pueden manipular cuáles de los comando se almacenarán o se mostrarán.

*** 

Ejecuta algunos comandos y luego ejecuta el comando 

`history`:

**Recuerda:** El comando `date` imprimirá la fecha y la hora en el sistema. El comando `clear` borra la pantalla.

El resultado debe ser similar al siguiente:
![[Pasted image 20240402112318.png]]

Para ver un número limitado de comandos, el comando `history` puede tomar un número como un parámetro para mostrar exactamente ese número de entradas recientes. Introduce el siguiente comando para mostrar los últimos cinco comandos de tu historial:

history 5

El resultado debe ser similar al siguiente:
![[Pasted image 20240402121716.png]]

Para ejecutar un comando, introduce el signo de exclamación y el número de la lista del historial. Por ejemplo, para ejecutar el comando número 94 en la lista del historial, tienes que ejecutar lo siguiente:

!18
![[Pasted image 20240402121836.png]]

A continuación, experimenta con el acceso a tu historial utilizando las **teclas de flecha hacia arriba** y **teclas de flecha hacia abajo**. Mantén presionada la tecla de flecha arriba hasta encontrar un comando que quieras ejecutar. Si fuera necesario, utiliza otras teclas para editar el comando y, a continuación, presiona **Entrar** para ejecutar el comando.

Algunos ejemplos adicionales del `history`:

| Ejemplo     | Significado                                                                |
| ----------- | -------------------------------------------------------------------------- |
| `history 5` | Muestra los últimos cinco comandos de la lista del historial               |
| `!!`        | Ejecuta el último comando otra vez                                         |
| `!-5`       | Ejecuta el quinto comando desde la parte inferior de la lista de historial |
| `!ls`       | Ejecuta el comando `ls` más reciente                                       |

[[La sintaxis de la Línea de Comandos]]
[[bash]]