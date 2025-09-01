TCP/IP Model Mapped to SOC Operations

[Image Placeholder: TCP/IP Model Diagram with Layers]

The TCP/IP model is the backbone of modern networking, describing how data flows across interconnected systems. For a SOC (Security Operations Center) analyst, this model is more than just theory — it is a map of visibility points, log sources, and attack surfaces. By aligning each layer with SOC responsibilities, analysts can effectively detect, investigate, and respond to security incidents.

🔹 1. Application Layer

Protocols: HTTP/HTTPS, DNS, SMTP, FTP, SSH

[Image Placeholder: Application Layer Attack Examples (Phishing, SQLi, DNS Tunneling)]

SOC Visibility:

Web server logs (Apache, Nginx, IIS)

Proxy and firewall logs for URL filtering

DNS query logs for suspicious lookups

Email gateway logs for phishing attempts

Common Attacks:

Phishing → Malicious email headers, attachments

Web Exploits → SQL injection, XSS, RCE

DNS Exfiltration → Suspicious long or repetitive queries

SOC Tools Used: SIEM (Splunk, QRadar, ELK), WAF, Email Security Gateways

🔹 2. Transport Layer

Protocols: TCP, UDP

[Image Placeholder: TCP 3-Way Handshake + SYN Flood Illustration]

SOC Visibility:

NetFlow/PCAP analysis (source & destination ports)

IDS/IPS logs on abnormal port usage

Authentication logs for repeated failed connections

Common Attacks:

DDoS (SYN/UDP Floods) → Overwhelms services

Port Scanning → Recon by attackers

Brute Force Attempts → SSH, RDP, or database logins

SOC Tools Used: Zeek, Suricata, Snort, Firewall/IPS logs

🔹 3. Internet Layer

Protocols: IP, ICMP

[Image Placeholder: IP Packet Flow + ICMP Ping Sweep Diagram]

SOC Visibility:

IP reputation (blacklists, TOR exit nodes, geo anomalies)

VPN and firewall logs (unusual IP changes, tunneling)

ICMP monitoring for unusual traffic

Common Attacks:

IP Spoofing → Evade attribution

ICMP Tunneling → Hidden communication channels

Lateral Movement → Across subnets/IP ranges

SOC Tools Used: Threat intelligence feeds, SIEM correlation, IDS signatures

🔹 4. Network Access Layer

Protocols: Ethernet, ARP, Wi-Fi, MAC addressing

[Image Placeholder: ARP Spoofing / Evil Twin Wi-Fi Attack Diagram]

SOC Visibility:

ARP cache monitoring for anomalies

NAC (Network Access Control) logs for rogue devices

Wireless logs for unauthorized access points

Common Attacks:

ARP Poisoning (MITM) → Redirect traffic

MAC Flooding → Overwhelm switches

Evil Twin Wi-Fi → Rogue AP impersonation

SOC Tools Used: Wireshark, Cisco ISE, WIDS/WIPS, ARPWatch

📌 SOC Analyst Takeaway

[Image Placeholder: SOC Workflow Diagram (Logs → Correlation → Detection → Response)]

The TCP/IP model provides SOC analysts with a structured way to:

Correlate logs across multiple layers

Detect anomalies in traffic flow and session behavior

Map Indicators of Compromise (IOCs) to specific layers

Implement defense-in-depth, ensuring attacks are blocked or detected at multiple points

In practice, a SOC analyst never looks at a packet or log entry in isolation — instead, they see it as part of a layered puzzle. Understanding where an attack manifests in the TCP/IP model makes detection and response faster, sharper, and more accurate.
