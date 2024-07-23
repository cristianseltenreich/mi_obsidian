El comando `find` en Linux es una herramienta poderosa que te permite buscar archivos y directorios en tu sistema de archivos. Aquí tienes una breve descripción y algunos ejemplos de las opciones más útiles:

- `find . -name "nombre"`: Este comando buscará en el directorio actual (.) y todos sus subdirectorios archivos cuyo nombre coincida con “nombre”. Por ejemplo, `find . -name "file.txt"` buscará un archivo llamado `file.txt` en el directorio actual y todos sus subdirectorios.
    
- `find /ruta -type f`: Este comando buscará todos los archivos regulares en la ruta especificada. Por ejemplo, `find /home/user -type f` buscará todos los archivos regulares en el directorio `/home/user`.
    
- `find /ruta -type d`: Este comando buscará todos los directorios en la ruta especificada. Por ejemplo, `find /home/user -type d` buscará todos los directorios en `/home/user`.
    
- `find . -mtime -n`: Este comando buscará archivos en el directorio actual que hayan sido modificados en los últimos n días. Por ejemplo, `find . -mtime -7` buscará archivos que hayan sido modificados en los últimos 7 días.
    
- `find . -size +nM`: Este comando buscará archivos en el directorio actual que sean mayores que n megabytes. Por ejemplo, `find . -size +100M` buscará archivos que sean mayores de 100 megabytes.

- `-name "nombre"`: Busca archivos cuyo nombre coincide exactamente con “nombre”. Por ejemplo, `find . -name "file.txt"` buscará un archivo llamado `file.txt` en el directorio actual y todos sus subdirectorios.
    
- `-iname "nombre"`: Similar a `-name`, pero ignora las diferencias entre mayúsculas y minúsculas. Por ejemplo, `find . -iname "file.txt"` buscará `file.txt`, `File.txt`, `FILE.TXT`, etc.
    
- `-perm 644`: Busca archivos con permisos específicos. Por ejemplo, `find . -perm 644` buscará todos los archivos en el directorio actual y subdirectorios con permisos `644` (propietario puede leer y escribir, grupo y otros solo pueden leer).
    
- `-atime n`: Busca archivos accedidos hace `n`*24 horas. Por ejemplo, `find . -atime 7` buscará archivos que fueron accedidos hace exactamente 7 días.
    
- `-mtime n`: Busca archivos modificados hace `n`*24 horas. Por ejemplo, `find . -mtime 7` buscará archivos que fueron modificados hace exactamente 7 días.
    
- `-amin n`: Similar a `-atime`, pero en minutos. Por ejemplo, `find . -amin 60` buscará archivos que fueron accedidos hace exactamente 60 minutos.
    
- `-mmin n`: Similar a `-mtime`, pero en minutos. Por ejemplo, `find . -mmin 60` buscará archivos que fueron modificados hace exactamente 60 minutos.
    
- `-size +nM`: Busca archivos mayores que `n` megabytes. Por ejemplo, `find . -size +100M` buscará archivos que sean mayores de 100 megabytes.
    
- a opción `-type` en el comando `find` se utiliza para buscar archivos de un tipo específico. Aquí tienes una breve descripción y algunos ejemplos:

- `find . -type f`: Este comando buscará todos los archivos regulares en el directorio actual y sus subdirectorios.
    
- `find . -type d`: Este comando buscará todos los directorios en el directorio actual y sus subdirectorios.
    
- `find . -type l`: Este comando buscará todos los enlaces simbólicos en el directorio actual y sus subdirectorios.
    

	Por ejemplo, si quieres buscar todos los archivos de texto en el directorio actual y sus subdirectorios, puedes usar el comando `find . -type f -name "*.txt"`. Esto buscará todos los archivos (debido a `-type f`) que terminen en `.txt` en el directorio actual y sus subdirectorios.


[[La sintaxis de la Línea de Comandos]]