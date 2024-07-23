Para iniciar un proceso en background se utiliza el símbolo & 

$ comando &
![[Pasted image 20240429201650.png]]

### Para ver la lista de procesos corriendo en background:

$ jobs
![[Pasted image 20240429201718.png]]

### Para traer un proceso al frente 

$ fg %nro_job

Luego para enviar el proceso a segundo plano debo detenerlo

1. Mientras el proceso está en ejecución, presiono `Ctrl+Z` para detenerlo (pasará al estado “Stopped”).
2. Luego, uso el comando `bg %1` para enviarlo de vuelta al segundo plano!!

![[Pasted image 20240429202222.png]]