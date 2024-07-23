Las prioridades en Linux se manejan con un valor entre -20 (prioridad más alta) a 19 (prioridad más baja).

0 es la prioridad por defecto.

Para correr un proceso con un prioridad 15: 

$ nice -n 15 comando 

Si queremos modificar la prioridad de un proceso que ya se encuentra corriendo: 

$ renice prioridad PID 

Solo root puede correr un proceso con mayor prioridad de la normal o aumentar la prioridad de un proceso.