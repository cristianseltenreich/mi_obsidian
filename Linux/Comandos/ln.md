El comando `ln` en Linux se utiliza para crear enlaces entre archivos y directorios. Aquí tienes una breve descripción y algunos ejemplos:

- `ln origen destino`: Este comando crea un enlace duro. Por ejemplo, `ln file1.txt link1` crea un enlace duro llamado `link1` al archivo `file1.txt`.
    
- `ln -s origen destino`: Este comando crea un enlace simbólico (también conocido como un “shortcut” o “alias”). Por ejemplo, `ln -s file1.txt link1` crea un enlace simbólico llamado `link1` al archivo `file1.txt`.
    

Es importante recordar que un enlace duro es esencialmente una referencia adicional al mismo archivo, mientras que un enlace simbólico es un archivo separado que apunta al archivo original. Si eliminas el archivo original, un enlace duro seguirá funcionando, pero un enlace simbólico se romperá.


[[La sintaxis de la Línea de Comandos]]