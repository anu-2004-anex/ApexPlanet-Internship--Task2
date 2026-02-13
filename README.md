🔐 **ApexPlanet Cybersecurity Internship – Task 2**
Network Security & Scanning
📅 Internship Phase

Days 13 – 24

🎯** Objective**

The objective of Task-2 is to gain hands-on experience in:

Network reconnaissance

Port scanning and service enumeration

Vulnerability assessment

Packet capture and analysis

Basic firewall rule configuration

All testing was conducted in a controlled lab environment using Kali Linux and a vulnerable target machine (Metasploitable2).

🖥 **Lab Environment**
Component	             Details
Attacker Machine-->	Kali Linux (VirtualBox)
Target Machine-->	Metasploitable2
Network Mode--->	NAT / Bridged Adapter
Tools Used	Nmap, Wireshark, Netcat, OpenVAS (optional), iptables
🧩 1️⃣** Reconnaissance**
🔎 Passive Reconnaissance

Gathered domain and IP information without directly interacting aggressively with the target.

**Commands Used:
whois <target-ip>
nslookup <target-ip>
ping <target-ip>**

Findings:

Target IP identified

Host availability verified

Basic DNS information collected

🔎 Active Reconnaissance

Performed controlled interaction with the target machine.

Commands Used:
nc <target-ip> 80


✔ Verified open HTTP service
✔ Confirmed active host response

🧩 2️⃣** Port & Service Scanning (Nmap)**

Used Nmap to identify open ports, services, and operating system details.

🔹 TCP SYN Scan
**nmap -sS <target-ip>**


✔ Detected open ports
✔ Identified listening services

🔹 Service Version Detection
**nmap -sV <target-ip>**


✔ Determined running service versions
✔ Identified outdated services

🔹 OS Detection
**nmap -O <target-ip>**


✔ Detected operating system fingerprint

🔹 Vulnerability Scan (Nmap Scripts)
**nmap --script vuln <target-ip>
**

✔ Detected potential security vulnerabilities
✔ Identified exposed services

🧩 3️⃣ **Vulnerability Assessment**

Vulnerability scanning revealed:

Outdated service versions

Potential exploit paths

Misconfigured services

Exposed ports

Severity levels categorized as:

Critical

High

Medium

Low

(Optional: OpenVAS scan performed for deeper analysis.)

🧩 4️⃣** Packet Analysis (Wireshark)**

Captured live network traffic during scanning activity.

🔹 Traffic Observed:

TCP SYN packets

Three-way handshake (SYN → SYN-ACK → ACK)

DNS queries

HTTP traffic

🔹 Filters Used:
tcp
dns
http
ftp


✔ Verified scanning activity
✔ Observed packet flow structure
✔ Analyzed protocol headers

🧩 5️⃣ **Firewall Configuration (iptables)**

Checked existing firewall rules:

sudo iptables -L


Blocked specific port:

sudo iptables -A INPUT -p tcp --dport 22 -j DROP


Verified rule:

sudo iptables -L


✔ Successfully modified firewall rules
✔ Understood traffic filtering basics

📊 **Key Observations**

Multiple open ports were discovered

Some services were outdated and vulnerable

TCP handshake process clearly observed

Vulnerability scripts detected exploitable services

Firewall rules effectively controlled traffic

📂 Repository Structure
TASK-2-Network-Security-Scanning
│
├── Screenshots/
│   ├── recon.png
│   ├── nmap_scan.png
│   ├── vuln_scan.png
│   ├── wireshark_capture.png
│   └── firewall_rules.png
│
├── scan_report.md
├── vulnerability_analysis.md
└── README.md

🎥 Demonstration Video

A 5-minute demo video includes:

Nmap scanning demonstration

Vulnerability findings explanation

Wireshark packet capture

Firewall rule configuration

Video link available on LinkedIn Featured section.

⚠ **Disclaimer**

**All activities were performed in a controlled lab environment using a deliberately vulnerable virtual machine (Metasploitable2).
No unauthorized systems or real-world networks were targeted.**

👩‍💻 Author

**Anamika B Pillai
B.Tech CSE (Data Science)
Cybersecurity Intern – ApexPlanet**

Passionate about Cybersecurity, AI & Network Security

🏁 **Conclusion**

Task-2 provided practical exposure to:

Ethical scanning methodologies

Vulnerability detection techniques

Packet inspection fundamentals

Basic firewall configuration

This hands-on implementation strengthened foundational knowledge in network security operations.
