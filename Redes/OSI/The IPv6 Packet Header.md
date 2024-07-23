There are eight fields in the IPv6 packet header, as shown in the figure.

**IPv6 Packet Header**
![[Pasted image 20240229160030.png]]

Version
- This field contains a 4-bit binary value set to 0110 that identifies this as an IPv6 packet.
Traffic Class
- This 8-bit field is equivalent to the IPv4 Differentiated Services (DS) field.
Flow Label
- This 20-bit field suggests that all packets with the same flow label receive the same type of handling by routers.

***

Payload Length
- This 16-bit field indicates the length of the data portion or payload of the IPv6 packet.
Next Header
- This 8-bit field is equivalent to the IPv4 Protocol field.
- It indicates the data payload type that the packet is carrying, enabling the network layer to pass the data to the appropriate upper-layer protocol.
Hop Limit
- This 8-bit field replaces the IPv4 TTL field.
- This value is decremented by a value of 1 by each router that forwards the packet.
- When the counter reaches 0, the packet is discarded, and an ICMPv6 Time Exceeded message is forwarded to the sending host, indicating that the packet did not reach its destination because the hop limit was exceeded.
Source IPv6 Address
- This 128-bit field identifies the IPv6 address of the sending host.
Destination IPv6 Address
- This 128-bit field identifies the IPv6 address of the receiving host.

An IPv6 packet may also contain extension headers (EH) that provide optional network layer information. Extension headers are optional and are placed between the IPv6 header and the payload. EHs are used for fragmentation, security, to support mobility, and more.

Unlike IPv4, routers do not fragment routed IPv6 packets.



Tags
[[The IPv4 Packet Header]]
[[Network security]]
[[Protocolos modelos OSI - TCP & IP]]
[[IPv4 and IPv6 threats]]
