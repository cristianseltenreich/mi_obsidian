El comando `cp` en Linux se utiliza para copiar archivos y directorios. Aquí tienes una breve descripción y algunos ejemplos:

- `cp origen destino`: Este comando copia el archivo o directorio de `origen` al `destino`. Por ejemplo, `cp file1.txt file2.txt` copiará `file1.txt` a `file2.txt`.
    
- `cp -r origen destino`: Este comando copia un directorio y todo su contenido (archivos y subdirectorios) de `origen` a `destino`. Por ejemplo, `cp -r dir1 dir2` copiará el directorio `dir1` y todo su contenido al directorio `dir2`.
    
- `cp -i origen destino`: Este comando solicita confirmación antes de sobrescribir el archivo de `destino`. Por ejemplo, `cp -i file1.txt file2.txt` te pedirá confirmación antes de sobrescribir `file2.txt`.
    
- `cp -u origen destino`: Este comando solo copia el archivo de `origen` al `destino` si el archivo de `origen` es más reciente que el archivo de `destino`, o si el archivo de `destino` no existe. Por ejemplo, `cp -u file1.txt file2.txt` solo sobrescribirá `file2.txt` si `file1.txt` es más reciente.


[[La sintaxis de la Línea de Comandos]]