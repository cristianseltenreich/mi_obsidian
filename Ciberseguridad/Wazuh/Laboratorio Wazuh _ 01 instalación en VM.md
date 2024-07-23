## Instalación de Wazuh en VM

La manera más sencilla y práctica es descargar la imágen ova de wazuh, que tiene todo lo necesario para funcionar en el ambiente de laboratorio que queremos montar.

Debemos descargar la imágen del sitio oficial de Wazuh, click en este enlace: [Máquina virtual (OVA) - Alternativas de instalación (wazuh.com)](https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html)

![[Pasted image 20240721222823.png]]


## Máquina virtual (OVA)

Wazuh proporciona una imagen de máquina virtual predefinida en formato Open Virtual Appliance (OVA). Esto se puede importar directamente a VirtualBox u otros sistemas de virtualización compatibles con OVA. Tenga en cuenta que esta máquina virtual solo se ejecuta en sistemas de 64 bits. No proporciona alta disponibilidad y escalabilidad listas para usar. Sin embargo, se pueden implementar mediante [la implementación distribuida](https://documentation.wazuh.com/current/installation-guide/index.html).

Descargue el [dispositivo virtual (OVA),](https://packages.wazuh.com/4.x/vm/wazuh-4.8.1.ova) que contiene los siguientes componentes:

> - Amazon Linux 2
>     
> - Administrador de Wazuh 4.8.1
>     
> - Indexador de Wazuh 4.8.1
>     
> - Filebeat-OSS 7.10.2
>     
> - Panel de control de Wazuh 4.8.1
>     

## Lista de paquetes[Enlace permanente a este titular](https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html#packages-list "Permalink to this headline")

|Distribución|Arquitectura|Formato de máquina virtual|Versión|Paquete|
|---|---|---|---|---|
|Amazon Linux 2|64 bits|OVA|4.8.1|[wazuh-4.8.1.ova](https://packages.wazuh.com/4.x/vm/wazuh-4.8.1.ova) ([sha512](https://packages.wazuh.com/4.x/checksums/wazuh/4.8.1/wazuh-4.8.1.ova.sha512))|

## Requisitos de hardware

Los siguientes requisitos deben cumplirse antes de que la máquina virtual de Wazuh se pueda importar a un sistema operativo host:

- El sistema operativo host tiene que ser un sistema de 64 bits.    
- La virtualización de hardware debe estar habilitada en el firmware del host.    
- Se debe instalar una plataforma de virtualización, como VirtualBox, en el sistema host.    

De forma predeterminada, la máquina virtual de Wazuh se configura con las siguientes especificaciones:

| Componente       | CPU (núcleos) | Memoria RAM (GB) | Almacenamiento (GB) |
| ---------------- | ------------- | ---------------- | ------------------- |
| Wazuh v4.8.1 OVA | 4             | 8                | 50                  |

Sin embargo, esta configuración de hardware se puede modificar en función del número de puntos de conexión protegidos y de los datos de alerta indexados. Puede encontrar más información sobre los requisitos [aquí](https://documentation.wazuh.com/current/quickstart.html).

## Importar y acceder a la máquina virtual

1. Importe el OVA a la plataforma de virtualización.    
![[Pasted image 20240721224257.png]]

![[Pasted image 20240721224101.png]]

2. Si está utilizando VirtualBox, configure el controlador gráfico. Al establecer otro controlador gráfico, se congela la ventana de la máquina virtual.`VMSVGA`    

    1. Seleccione la máquina virtual importada.        
    2. Haga clic en **Configuración** > **Pantalla**        
    3. En **Controlador gráfico**, seleccione la opción.`VMSVGA`        
     
![[Pasted image 20240721224548.png]]

3. Encienda la máquina.    
4. Acceda a la máquina virtual con el siguiente usuario y contraseña. Puede utilizar la plataforma de virtualización o acceder a ella a través de SSH.    
![[Pasted image 20240721225028.png]]

    user: wazuh-user
    password: wazuh
    
![[Pasted image 20240721225537.png]]
Se ha desactivado el inicio de sesión de usuario SSH; sin embargo, conserva los privilegios de sudo. La escalada de privilegios raíz se puede lograr ejecutando el siguiente comando:`root``wazuh-user`
    
    sudo -i
    

## Accede al panel de control de Wazuh

Luego de iniciar la máquina virtual, ya se puede acceder al panel de control de Wazuh desde un navegador (en mi caso utilizo firefox de mi lubuntu virtual) 

Se debe ingresar con la ip del servidor a la url del panel de Wazuh:

> URL: https://<wazuh_server_ip>


Puede encontrar la ip del server wazuh escribiendo el siguiente comando en la máquina virtual:`<wazuh_server_ip>`

> ip a
> 
![[Pasted image 20240721230056.png]]

Se deben utilizar las siguientes credenciales:

> user: admin
> password: admin

![[Pasted image 20240721225955.png]]


Como se puede observar, luego de ingresar las credenciales ya estárá dentro del panel web de Wazuh!!

![[Pasted image 20240721232401.png]]

## Archivos de configuración

Todos los componentes incluidos en esta imagen virtual están configurados para funcionar de forma inmediata, sin necesidad de modificar ninguna configuración. Sin embargo, todos los componentes se pueden personalizar por completo. Estas son las ubicaciones de los archivos de configuración:

> - Wazuh manager: `/var/ossec/etc/ossec.conf`
>     
> - Wazuh indexer: `/etc/wazuh-indexer/opensearch.yml`
>     
> - Filebeat-OSS: `/etc/filebeat/filebeat.yml`
>     
> - Wazuh dashboard:
>     
>     > - `/etc/wazuh-dashboard/opensearch_dashboards.yml`
>     >     
>     > - `/usr/share/wazuh-dashboard/data/wazuh/config/wazuh.yml`
>     >     
>     



## Configuración horaria de VirtualBox

En caso de usar VirtualBox, una vez que se importa la máquina virtual, puede encontrarse con problemas causados por el sesgo de tiempo cuando VirtualBox sincroniza la hora de la máquina invitada. Para evitar esta situación, habilite la opción en la pestaña de la configuración de la máquina virtual.

`Hardware Clock in UTC Time``System`

**Nota**
De forma predeterminada, el tipo de interfaz de red se establece en Adaptador puenteado. La máquina virtual intentará obtener una dirección IP del servidor DHCP de red. Como alternativa, se puede establecer una dirección IP estática configurando los archivos de red adecuados en el sistema operativo Amazon Linux en el que se basa la máquina virtual.

Una vez que la máquina virtual está importada y en ejecución, el siguiente paso es [implementar los agentes de Wazuh](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html) en los sistemas que se van a supervisar.

## Actualización de la máquina virtual

La máquina virtual se puede actualizar como una instalación tradicional:

> - [Actualización de los componentes centrales de Wazuh](https://documentation.wazuh.com/current/upgrade-guide/upgrading-central-components.html)
>