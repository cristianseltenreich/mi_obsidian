Por lo general, introduces un solo comando y lo ejecutas presionando **Entrar**. El shell Bash ofrece tres estados diferentes que se pueden utilizar para separar varios comandos escritos juntos.

El separador más simple es **el punto y coma** (`;`). El uso de punto y coma entre múltiples comandos les permite ejecutarse el uno tras el otro de forma secuencial de la izquierda a la derecha.

Los caraceters `&&` crean una lógica e instrucción. Los comandos separados por `&&` se ejecutan de manera condicional. Si el comando a la izquierda de `&&` tiene éxito, entonces el comando a la derecha de `&&` también será ejecutado. Si el comando a la izquierda de `&&` falla, entonces el comando a la derecha de la `&&` no se ejecuta.

Los caracteres `||` crean una lógica o una instrucción que también causa una ejecución condicional. Cuando los comandos están separados por `||`, entonces sólo si el comando a la izquierda falla, el comando a la derecha de `||` se ejecuta. Si el comando a la izquierda de `||` tiene éxito, entonces el comando a la derecha de la `||` no se ejecuta.

Para ver cómo funcionan instrucciones de control, podrás utilizar dos ejecutables especiales: `true` y `false`. El ejecutable `true` siempre tiene éxito cuando se ejecuta, mientras que, el ejecutable `false` siempre falla. Si bien esto no te puede proporcionar ejemplos realistas acerca de cómo `&&` y `||` funcionan, proporciona un medio para demostrar cómo funcionan sin tener que introducir nuevos comandos.

***

Ejecuta los tres siguientes comandos juntos separadas por punto y coma:

echo Hello; echo Linux; echo Student

Como puedes ver en la salida, los tres comandos se ejecutan de forma secuencial:
![[Pasted image 20240402110145.png]]

Ahora, pon juntos los tres comandos separados por punto y coma, donde el primer comando se ejecuta con un resultado de fallo:

false; echo Not; echo Conditional

El resultado debe ser similar al siguiente:
![[Pasted image 20240402110307.png]]

Ten en cuenta que en el ejemplo anterior, los tres comandos se ejecutan a pesar de que el primero falle. Aunque no lo puedes ver en la salida del comando `false`, éste se ejecutó. Sin embargo, cuando los comandos están separadas por el carácter `;`, son completamente independientes entre sí.

A continuación, utiliza «logical and» («y» lógico) y para separar los comandos:

echo Start && echo Going && echo Gone

El resultado debe ser similar al siguiente:
![[Pasted image 20240402110437.png]]

Debido a que cada instrucción `echo` se ejecuta correctamente, se proporciona un valor de retorno de éxito, permitiendo que la siguiente instrucción también se ejecute.

*** 
Usa «y lógico» con un comando que falla como se muestra a continuación:

echo Success && false && echo Bye

El resultado debe ser similar al siguiente:

**sysadmin@localhost:~$** echo Success && false && echo Bye
Success
**sysadmin@localhost:~$**

El primer comando `echo` se ejecuta correctamente y vemos su salida. El comando `false` se ejecuta con un resultado de fallo, por lo que el último comando `echo` no se ejecuta.

Usa «y lógico» con un comando que falla como se muestra a continuación:

echo Success && false && echo Bye

El resultado debe ser similar al siguiente:
![[Pasted image 20240402110845.png]]

El primer comando `echo` se ejecuta correctamente y vemos su salida. El comando `false` se ejecuta con un resultado de fallo, por lo que el último comando `echo` no se ejecuta.

***
Los carácteres `or` que separan los siguientes comandos muestra cómo el fracaso antes de la instrucción `or` provoca que el siguiente comando sea ejecutado; sin embargo, la primera instrucción exitosa hace que el comando no se ejecute:

false || echo Fail Or
true || echo Nothing to see here

El resultado debe ser similar al siguiente:
![[Pasted image 20240402111054.png]]
![[Pasted image 20240402111147.png]]


[[La sintaxis de la Línea de Comandos]]
[[bash]]