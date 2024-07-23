Threat actors use Internet Control Message Protocol (ICMP) echo packets (pings) to discover subnets and hosts on a protected network, to generate DoS flood attacks, and to alter host routing tables.

[[ICMP]] was developed to carry diagnostic messages and to report error conditions when routes, hosts, and ports are unavailable. ICMP messages are generated by devices when a network error or outage occurs. The ping command is a user-generated ICMP message, called an echo request, that is used to verify connectivity to a destination.

Threat actors use ICMP for reconnaissance and scanning attacks. This enables them to launch information-gathering attacks to map out a network topology, discover which hosts are active (reachable), identify the host operating system (OS fingerprinting), and determine the state of a firewall.

Threat actors also use ICMP for DoS and DDoS attacks, as shown in the ICMP flood attack in the figure.

![[Pasted image 20240306155342.png]]

**Note:** ICMP for IPv4 (ICMPv4) and ICMP for IPv6 (ICMPv6) are susceptible to similar types of attacks.

The following lists common ICMP messages of interest to threat actors:

- ICMP echo request and echo reply
	This is used to perform host verification and DoS attacks.
- ICMP unreachable
	This is used to perform network reconnaissance and scanning attacks.
- ICMP mask reply	
	This is used to map an internal IP network.
- ICMP redirects
	This is used to [[lure]] a target host into sending all traffic through a compromised device and create a MiTM attack.
- ICMP router discovery
	This is used to inject [[bogus]] route entries into the routing table of a target host.

Networks should have strict ICMP access control list (ACL) filtering on the network edge to avoid ICMP probing from the internet. Security analysts should be able to detect ICMP-related attacks by looking at captured traffic and log files. In the case of large networks, security devices, such as firewalls and intrusion detection systems (IDS), should detect such attacks and generate alerts to the security analysts.

tags
[[IP Vulnerabilities]]
[[Ataques DoS -denegación de servicio-]]
[[Denial-of-Service (DoS) attacks]]