
The fields in the IPv4 packet header are shown in the figure.

**IPv4 Packet Header**

![[Pasted image 20240229141321.png]]


#### Version
- Contains a 4-bit binary value set to 0100 that identifies this as an IPv4 packet.
#### Internet Header length
- A 4-bit field containing the length of the IP header.
- The minimum length of an IP header is 20 bytes.
#### Differentiated Services or DiffServ (DS)
- Formerly called the Type of Service (ToS) field, the DS field is an 8-bit field used to determine the priority of each packet.
- The six most significant bits of the DiffServ field are the Differentiated Services Code Point (DSCP).
- The last two bits are the Explicit Congestion Notification (ECN) bits.
#### Total length
- Specifies the length of the IP packet including the IP header and the user data.
- The total length field is 2 bytes, so the maximum size of an IP packet is 65,535 bytes; however, packets are much smaller in practice.
 
***
#### Identification, Flag, and Fragment offset
- As an IP packet moves through the internet, it might need to cross a route that cannot handle the size of the packet.
- The packet will be divided, or fragmented, into smaller packets and reassembled later.
- These fields are used to fragment and reassemble packets.
#### Time-to-Live (TTL)
- Contains an 8-bit binary value that is used to limit the lifetime of a packet.
- The packet sender sets the initial TTL value, and it is decreased by one each time the packet is processed by a router.
- If the TTL field decrements to zero, the router discards the packet and sends an Internet Control Message Protocol (ICMP) Time Exceeded message to the source IP address.
#### Protocol
- Field is used to identify the next level protocol.
- This 8-bit binary value indicates the data payload type that the packet is carrying, which enables the network layer to pass the data to the appropriate upper-layer protocol.
- Common values include ICMP (1), TCP (6), and UDP (17).
#### Header checksum
- A value that is calculated based on the contents of the IP header.
- Used to determine if any errors have been introduced during transmission.
#### Source IPv4 Address
- Contains a 32-bit binary value that represents the source IPv4 address of the packet.
- The source IPv4 address is always a unicast address.
#### Destination IPv4 Address
- Contains a 32-bit binary value that represents the destination IPv4 address of the packet.
#### Options and Padding
- This is a field that varies in length from 0 to a multiple of 32 bits.
- If the option values are not a multiple of 32 bits, 0s are added, or padded, to ensure that this field contains a multiple of 32 bits.

tags
[[The IPv6 Packet Header]]
[[Network security]]
[[Protocolos modelos OSI - TCP & IP]]
[[IPv4 and IPv6 threats]]
