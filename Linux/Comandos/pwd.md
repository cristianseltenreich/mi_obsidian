El comando `pwd` se utiliza para mostrar tu «ubicación» actual o el directorio de «trabajo» actual. Introduce el siguiente comando para visualizar el directorio de trabajo:

pwd

El resultado debe ser similar al siguiente:
![[Pasted image 20240318195738.png]]

El directorio actual en el ejemplo anterior es `/home/sysadmin`. Esto también se conoce como tu directorio home , una ubicación especial en la que controlas los archivos y al que los otros usuarios normalmente no tienen acceso. De forma predeterminada, este directorio tiene el mismo nombre que tu nombre de usuario y se encuentra bajo el directorio `/home`.

Como puedes ver en la salida del comando, `/home/sysadmin`, Linux utiliza la barra diagonal `/` para separar los directorios para crear lo que se denomina ruta. La barra diagonal inicial representa el directorio de nivel superior, conocido como el directorio root . Más información sobre los archivos, directorios y caminos se presentará en los laboratorios posteriores.

El tilde `~`  que ves en el prompt también está indicando cuál es el directorio actual. Este carácter es una forma de «acceso directo» para representar tu home.

**Curiosidad**
El comando `pwd` significa «imprimir el directorio de trabajo». A pesar de que las versiones modernas en realidad no «imprimen», las máquinas UNIX más antiguas no tenían monitores y la salida de los comandos iban a una impresora, de ahí el nombre divertido de `pwd`.

[[Linux]]
[[La sintaxis de la Línea de Comandos]]