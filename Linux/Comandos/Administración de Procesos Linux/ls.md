ls muestra la lista de archivos y directorios de la carpeta donde estoy parado

ls -l 

es la forma large donde muestra permisos dueño, grupo al que pertenece, tamaño fecha de creación y el nombre 

┌──(kali㉿Kali)-[~]
└─$ ls -l                                                                    
total 36
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Desktop
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Documents
drwxr-xr-x 2 kali kali 4096 Jul 13  2011 Downloads
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Music
drwxr-xr-x 2 kali kali 4096 Sep  3  2011 OTHER
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Pictures
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Public
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Templates
drwxr-xr-x 2 kali kali 4096 Jan 16 00:53 Videos


ls -a muestra además archivos ocultos 

┌──(kali㉿Kali)-[~]
└─$ ls -a                                                                    
.
..
.ICEauthority
.Xauthority
.bash_history
.bash_logout
.bashrc

. hace referencia al directorio actual
.. hacer referencia al directorio padre

Si creamos un archivo comenzando un punto por ej .archivooculto, este por defecto se crea oculto


[[La sintaxis de la Línea de Comandos]]