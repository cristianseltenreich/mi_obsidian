
El comando `mv` en Linux se utiliza para mover o renombrar archivos y directorios. Aquí tienes una breve descripción y algunos ejemplos:

- `mv origen destino`: Este comando mueve el archivo o directorio de `origen` al `destino`. Por ejemplo, `mv file1.txt dir1/` moverá `file1.txt` al directorio `dir1`.
    
- `mv -i origen destino`: Este comando solicita confirmación antes de sobrescribir el archivo de `destino`. Por ejemplo, `mv -i file1.txt file2.txt` te pedirá confirmación antes de sobrescribir `file2.txt`.
    
- `mv -u origen destino`: Este comando solo mueve el archivo de `origen` al `destino` si el archivo de `origen` es más reciente que el archivo de `destino`, o si el archivo de `destino` no existe. Por ejemplo, `mv -u file1.txt file2.txt` solo sobrescribirá `file2.txt` si `file1.txt` es más reciente.
    
- `mv -v origen destino`: Este comando muestra información detallada sobre lo que está haciendo. Por ejemplo, `mv -v file1.txt file2.txt` mostrará un mensaje indicando que `file1.txt` ha sido renombrado a `file2.txt`.

[[La sintaxis de la Línea de Comandos]]