[[Threat]]
[[Landscape]]

Part 1: Investigate a Network Configuration Vulnerability
Sometimes network security vulnerabilities can happen by accident. For example, forgetting to update server or host software may expose known vulnerabilities that could easily be mitigated with a simple update. Similarly, vulnerabilities may be introduced when a network device is not configured properly, or a device is defective. In this part, you will explore a vulnerability that results from a device that is not properly configured with security best practices.

Step 1: Use a guest network to gain access to other devices on the network.
a.     In Greenville, locate Smartphone 3 just outside of the Home location.

Mary is the owner of this smartphone. She is a friend of Bob who lives in the house. Mary is studying to eventually get a job in cybersecurity defense and is familiar with network penetration testing. She noticed that a guest wireless network is open and accessible by anyone. She connected to the guest network and used Nmap to run a scan, which can identify and discover details about all the active devices. One of the devices appears to be a webcam. Its IP address is 192.168.100.101.

b.     Click Smartphone 3, and then click Command Prompt. Enter the command ping 192.168.100.101. After one or two "Request timed out" messages, the remaining pings should be successful.

![[Pasted image 20240218105621.png]]

Mary informs Bob that the network is very vulnerable to attack. Someone could take control of the webcam, for example, and watch video from inside the house. Bob invites Mary to come in, investigate the issue, and propose a solution.

