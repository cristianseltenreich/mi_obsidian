Introduce el siguiente comando para mostrar el valor de la variable `PATH`:

echo $PATH

El resultado debe ser similar al siguiente:

**sysadmin@localhost:~$** echo $PATH
/home/sysadmin/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games
**sysadmin@localhost:~$**

La variable `PATH` se visualiza mediante la colocación del carácter `$` delante del nombre de la variable.

Esta variable se utiliza para encontrar la ubicación de los comandos. Cada uno de los directorios mencionados anteriormente se buscan cuando ejecutas un comando. Por ejemplo, si intentas a ejecutar el comando `date`, el shell buscará el comando primero en el directorio `/home/sysadmin/bin`, luego en el directorio `/usr/local/sbin`  y así sucesivamente. Una vez el shell encuentra el comando `date`, «lo ejecuta».

[[bash]]
[[Linux]]
[[La sintaxis de la Línea de Comandos]]

