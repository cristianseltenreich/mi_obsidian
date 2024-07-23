Utiliza el comando `which` para determinar si existe un archivo ejecutable llamado `date` ubicado en un directorio que aparece en el valor `PATH`:

which date

El resultado debe ser similar al siguiente:
![[Pasted image 20240318200128.png]]

La salida del comando `which` te dice que cuando ejecutas el comando `date`, el sistema ejecutará el comando `/bin/date`. El comando `which` hace uso de la variable `PATH` para determinar la ubicación del comando `date`.

[[bash]]
[[Linux]]
