[[Foundations of Threat Hunting]]

These challenges result in a culture [[shift]] in the detection of threats.

We are mostly operating on the [[firefighting]] level, responding to alerts that are generated in your organization. We are performing actions in reactions to notifications of security tools, such as SIEM, EDR, and IPS. This is completely understandable In case of those [[triggers]] are relevant and help us to address important issues.

Yet, the only plan cannot be sitting around and waiting for notifications about something bad happening. We should be proactive and find malicious activities happening in your environment.

Starting with the first antivirus software, we are traditionally detecting Atomic IOCs, such as hash values, IP addresses, and domain names. However, we must start to detect adversary [[behavior]], tactics, techniques, and procedures (TTPs), and tools used by adversaries. At least, we have to detect their artifacts in network and hosts. 

Transitioning from reactive to proactive is slow. It can be difficult, and fallbacks to IOCs are understandable. So, how do we start climbing this pyramid and get away from solely focusing on IoC more towards to the top of the pyramid? The answer is threat hunting.