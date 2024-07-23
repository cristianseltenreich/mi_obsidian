La manipulación de archivos y directorios es una habilidad fundamental en sistemas operativos como Linux y Unix. A continuación, te presento algunos comandos básicos que te permitirán trabajar con archivos y directorios desde la línea de comandos:

1. **`head`**: Este comando muestra las primeras diez líneas de un archivo (o el número de líneas especificado). Por ejemplo, para ver las primeras cien bytes de un archivo llamado `filename.txt`, puedes usar `head -c 100 filename.txt`.
    
2. **`tail`**: El comando `tail` imprime las últimas diez líneas de un archivo por defecto. Si deseas limitar el número de líneas, puedes usar la opción `-n` seguida del número deseado. Por ejemplo, para ver las últimas 10 líneas de un archivo, escribe `tail filename.txt`. Si quieres ver solo las últimas cinco líneas, usa `tail -n 5 filename.txt`.
    
3. **`cat`**: El comando `cat` (concatenar) es ampliamente utilizado en sistemas Linux y Unix. Puedes usarlo para ver el contenido de uno o varios archivos, concatenarlos o redirigir la salida a la terminal. Por ejemplo, para mostrar el contenido del archivo `/etc/passwd`, ejecuta `cat /etc/passwd`.
    
4. **`grep`**: Este comando se utiliza para buscar una cadena de caracteres (expresión regular) en un archivo específico. Cuando encuentra una coincidencia, imprime la línea correspondiente. Es útil para buscar en archivos de registros grandes. Por ejemplo, para buscar la palabra “error” en un archivo llamado `logfile.txt`, usa `grep "error" logfile.txt`.
    
5. **`chmod`**: Con este comando, puedes controlar los permisos de un archivo o directorio en Linux. Hay tres tipos de permisos: para el propietario del archivo, para los miembros del grupo y para otros usuarios. Puedes agregar o quitar permisos según tus necesidades. Por ejemplo:
    
    - Para agregar permisos de lectura, escritura y ejecución al archivo `filename`, usa `chmod +rwx filename`.
    - Para eliminar permisos de escritura y ejecución de un directorio llamado `dirname`, ejecuta `chmod -wx dirname`.
    - Para permitir permisos ejecutables en un archivo, usa `chmod +x filename`.
6. **`logger`**: Esta herramienta te permite agregar mensajes al archivo `/var/log/syslog` desde la línea de comandos o desde otros archivos. Es útil para registrar eventos y errores. Por defecto, está instalada en la mayoría de las distribuciones de Linux. Puedes especificar prioridades, sistemas remotos y puertos syslog. Por ejemplo, para agregar un mensaje al registro, utiliza `logger "Mi mensaje aquí"`.

[[Operaciones y respuesta a incidentes de ciberseguridad (CompTIA Security+ SY0-601]]

