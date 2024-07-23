La **desinfección de datos** es un paso crucial en el ciclo de vida de la información. Cuando los datos llegan al final de su vida útil o se consideran triviales, obsoletos o redundantes, es fundamental eliminarlos de manera segura. **Blancco**, una empresa internacional de seguridad de datos especializada en el borrado de datos, define la desinfección de datos como el proceso deliberado, permanente e irreversible de eliminación o destrucción de datos almacenados en dispositivos de memoria para que sean irrecuperables. Un dispositivo desinfectado no contiene datos residuales utilizables, incluso con la ayuda de herramientas forenses avanzadas.

Según **Gartner**, líder mundial en investigación y asesoramiento, existen tres métodos para lograr la desinfección de datos:

1. **Destrucción física:** Implica dañar físicamente el dispositivo.
2. **Borrado criptográfico:** Utiliza algoritmos criptográficos para borrar los datos.
3. **Borrado de datos:** Consiste en sobrescribir los datos con patrones específicos.

Es importante distinguir estos métodos de otros enfoques que no garantizan la desinfección completa. Por ejemplo, los archivos eliminados de un disco duro magnético no se borran realmente; solo se marcan como disponibles para escritura. El uso de la herramienta de formato estándar de Windows también deja los sectores disponibles para su uso.

La **sobreescritura** es el método estándar para desinfectar un disco duro. Se realiza mediante herramientas de firmware de la unidad o programas de utilidad. Aunque una sola pasada de llenado de ceros puede dejar patrones recuperables, se recomienda una sobreescritura más segura con datos ceros, unos y un patrón pseudoaleatorio.

Desde 2001, las especificaciones **SATA** y **Serial Attached SCSI (SAS)** han incluido un comando **Secure Erase (SE)**. Este comando se puede invocar mediante utilidades de unidad o matriz, como **hdparm** en Linux. Sin embargo, para SSD, unidades híbridas, algunas unidades de memoria USB y tarjetas de memoria flash, los métodos de sobreescritura no son confiables debido a las rutinas de nivelación de desgaste en el controlador de la unidad. En los SSD, el comando SE marca todos los bloques como vacíos, y los recolectores de basura automáticos del firmware de la unidad realizan el borrado real de cada bloque con el tiempo. Si este proceso no se completa y no hay indicador de progreso, existe el riesgo de recuperación remanente, aunque esto requiere retirar los chips del dispositivo para analizarlos en un hardware especializado.

[[Operaciones y respuesta a incidentes de ciberseguridad (CompTIA Security+ SY0-601]]
