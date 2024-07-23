
---

Network Mapper (`Nmap`) es una herramienta de análisis de redes y auditoría de seguridad de código abierto escrita en C, C++, Python y Lua. Está diseñada para escanear redes e identificar qué hosts están disponibles en la red utilizando paquetes sin procesar, y servicios y aplicaciones, incluyendo el nombre y la versión, cuando sea posible. También puede identificar los sistemas operativos y las versiones de estos hosts. Además de otras funciones, Nmap también ofrece capacidades de escaneo que pueden determinar si los filtros de paquetes, cortafuegos o sistemas de detección de intrusiones (IDS) están configurados según sea necesario.


---
## Use Cases

Se trata de una de las herramientas más utilizadas por los administradores de redes y los especialistas en seguridad informática. Se utiliza para:

- Auditar los aspectos de seguridad de las redes
- Simular pruebas de penetración
- Comprobar los ajustes y configuraciones de cortafuegos e IDS
- Tipos de conexiones existentes
- Mapeo de redes
- Análisis de respuestas
- Identificación de puertos abiertos
- También evaluación de vulnerabilidades

---

## Nmap Architecture

Nmap offers many different types of scans that can be used to obtain various results about our targets. Basically, Nmap can be divided into the following scanning techniques:

- Descubrimiento de hosts
- Escaneado de puertos
- Enumeración y detección de servicios
- Detección de SO
- Interacción mediante scripts con el servicio objetivo (motor de scripts de Nmap)

---

## Syntax

La sintaxis de Nmap es bastante simple y tiene el siguiente aspecto:

```shell-session
cristianseltenreich@htb[/htb]$ nmap <scan types> <options> <target>
```

---

## Scan Techniques

Nmap ofrece diferentes técnicas de escaneo, realizando diversos tipos de conexiones y utilizando diferentes estructuras de paquetes para el proceso de envío. Aquí podemos ver todas las técnicas de escaneo que ofrece Nmap:

```
cristianseltenreich@htb[/htb]$ nmap --help

  -sS/sT/sA/sW/sM: TCP SYN/Connect()/ACK/Window/Maimon scans
  -sU: UDP Scan
  -sN/sF/sX: TCP Null, FIN, and Xmas scans
  --scanflags <flags>: Customize TCP scan flags
  -sI <zombie host[:probeport]>: Idle scan
  -sY/sZ: SCTP INIT/COOKIE-ECHO scans
  -sO: IP protocol scan
  -b <FTP relay host>: FTP bounce scan

```

Por ejemplo, el escaneo TCP-SYN (`-sS`) es una de las opciones por defecto a menos que hayamos definido otra cosa y es también uno de los métodos de escaneo más populares. Este método de escaneo permite escanear varios miles de puertos por segundo. El escaneo TCP-SYN envía un paquete con la bandera SYN y, por lo tanto, nunca completa el handshake de tres vías, lo que resulta en no establecer una conexión TCP completa al puerto escaneado.

- Si nuestro objetivo envía un paquete con la bandera `SYN-ACK` de vuelta al puerto escaneado, Nmap detecta que el puerto está `abierto`.
- Si el paquete recibe una bandera `RST`, es un indicador de que el puerto está `cerrado`.
- Si Nmap no recibe un paquete de vuelta, lo mostrará como "filtrado". Dependiendo de la configuración del cortafuegos, ciertos paquetes pueden ser descartados o ignorados por el firewall.


Veamos un ejemplo de un escaneo de este tipo:

```
cristianseltenreich@htb[/htb]$ sudo nmap -sS localhost

Starting Nmap 7.80 ( https://nmap.org ) at 2020-06-11 22:50 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000010s latency).
Not shown: 996 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
5432/tcp open  postgresql
5901/tcp open  vnc-1

Nmap done: 1 IP address (1 host up) scanned in 0.18 seconds
```

En este ejemplo, podemos ver que tenemos cuatro puertos TCP diferentes abiertos. En la primera columna, vemos el número del puerto. Luego, en la segunda columna, vemos el estado del servicio y qué tipo de servicio es.



[[Network Enumeration Whith Nmap]]