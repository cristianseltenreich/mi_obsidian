
IP was designed as a Layer 3 connectionless protocol. It provides the necessary functions to deliver a packet from a source host to a destination host over an interconnected system of networks. The protocol was not designed to track and manage the flow of packets. These functions, if required, are performed primarily by TCP at Layer 4.

IP makes no effort to validate whether the source IP address contained in a packet actually came from that source. For this reason, threat actors can send packets using a spoofed source IP address. In addition, threat actors can tamper with the other fields in the IP header to carry out their attacks. Therefore, it is important for security analysts to understand the different fields in both the IPv4 and IPv6 headers.

tags
[[The IPv6 Packet Header]]
[[The IPv4 Packet Header]]
[[Network security]]
[[Protocolos modelos OSI - TCP & IP]]
[[IP Vulnerabilities]]
