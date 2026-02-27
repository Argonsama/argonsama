## Hi there 👋
#disclaimer(This project is for educational purposes only. All testing was performed in a controlled environment or on authorized targets.)

**Task 1: Reconnaissance Tools**

• Recon-ng
1. Workspace Management
The screenshot demonstrates the use of the commands workspaces create, workspaces list, and workspaces load to manage a workspace named "Project CS".
Workspaces in Recon-ng are designed to logically separate and organize data based on different targets or projects. By creating a dedicated workspace for each engagement, reconnaissance data remains isolated and structured. This prevents data overlap between projects and helps maintain accuracy, organization, and data integrity throughout the penetration testing process.
2. Marketplace Integration
The screenshot shows the use of marketplace search and marketplace install commands to locate and install the google_site_web module within the framework.
Recon-ng operates as a modular Open Source Intelligence (OSINT) framework. The marketplace feature allows penetration testers to selectively install only the modules required for a specific assessment. This modular approach enhances flexibility, reduces unnecessary clutter, and ensures that the framework remains efficient and tailored to the engagement’s objectives.
3. Automated Information Gathering
The screenshot illustrates loading a module, configuring it by setting the SOURCE option to https://www.google.com/search?q=google.com, and executing the run command.
This process automates the collection of reconnaissance data, such as hostnames and subdomains, from search engine results. Automated information gathering significantly reduces manual effort and speeds up the intelligence-gathering phase. By identifying components of the target’s web infrastructure early, penetration testers can better understand the attack surface and plan a more strategic and effective security assessment.

<img width="1440" height="862" alt="4 (2)" src="https://github.com/user-attachments/assets/2a888ab2-fcba-4bfd-86f9-5e3df4d9ab70" />

• Nmap 
1. nmap -sV (Service Version Detection)
Identifies what services are running on open ports and detects their version numbers (e.g., Apache, SSH).
It helps to find outdated or vulnerable services.

<img width="902" height="280" alt="-sv" src="https://github.com/user-attachments/assets/0761802e-cdce-4c94-a16c-52b3f5c61957" />

2. nmap -O (Operating System Detection)
Attempts to identify the target’s operating system (e.g., Windows, Linux).
Very useful for understanding the system type and potential attack methods.

<img width="574" height="99" alt="-o" src="https://github.com/user-attachments/assets/02bda795-5a34-481f-9c2f-38a1bb5ae15c" />

3. nmap -A (Aggressive Scan)
Combines OS detection, service version detection, script scanning, and traceroute in one command.
➡️ Provides comprehensive information but is more intrusive.

<img width="877" height="403" alt="-A" src="https://github.com/user-attachments/assets/a614b2e2-c4b2-491d-a745-3c7d32572f32" />

• DNSRecon 

1. dns -d google.com

Performs basic DNS enumeration on the domain.
Retrieves information such as name servers, IP addresses, and basic DNS records.
<img width="1066" height="783" alt="-d" src="https://github.com/user-attachments/assets/1f1d023f-906a-40c6-84d2-4c2fdb735d3a" />

2. dns -d google.com -t axfr

Attempts a DNS zone transfer (AXFR).
If successful, it reveals all DNS records for the domain, which can expose internal infrastructure.
<img width="512" height="786" alt="-d -t" src="https://github.com/user-attachments/assets/78c00b3f-97a5-410c-8f3c-8b9cbf0b6e69" />

3. dns -r

Enables recursive or reverse DNS lookup.
Used to discover domain names linked to IP address ranges.
<img width="520" height="92" alt="-r" src="https://github.com/user-attachments/assets/cdcf9919-9531-4638-844e-b372b3588d1b" />

• Hping3 

1. hping3 -s -p <port> -c <count>

Sends a fixed number of packets to a specific port.
Used to test basic connectivity and port response.
<img width="706" height="348" alt="-s -p -c" src="https://github.com/user-attachments/assets/7cbb6234-9f3f-4fd2-bbb8-c3414aa8a919" />

2. hping3 -s -p <port> -c <count> -i <interval>

Sends packets with a controlled time interval between each packet.
Used to analyze network latency and packet timing behavior.

<img width="760" height="215" alt="-s -p -c -i" src="https://github.com/user-attachments/assets/bfe5482e-a50b-4b3e-ae16-b44e86532ad0" />

3. hping3 -S -p <port> --flood <target>

Sends continuous TCP SYN packets to port at high speed.
Used to stress-test firewalls or IDS/IPS systems.

![--flood](https://github.com/user-attachments/assets/28bb33cd-98bd-494e-9997-fb09551ca4ab)


**Task 2: Maintaining access tools**
• Powersploit
• Webshells
• Weevely 
• Dns2tcp 
• Cryptcat 

**Tools comparison**

>Comparison of Reconnaissance Tools
1. Recon-ng focuses on Open Source Intelligence (OSINT) gathering. It collects information from publicly available sources such as websites, search engines, and online databases. This tool is mainly used during the early reconnaissance phase of a cybersecurity assessment to gather preliminary information about a target. Recon-ng has a look and feel similar to the Metasploit Framework, reducing the learning curve for leveraging the framework

2. Nmap is used for network scanning and service detection. It identifies open ports, running services, and the operating system of a target machine. Nmap is commonly used for network mapping and vulnerability assessment to understand the structure and exposure of a network. Topics include subverting firewalls and intrusion detection systems, optimizing Nmap performance, and automating common networking tasks with the Nmap Scripting Engine. Nmap runs on Windows, Linux, and Mac OS X. 

3. hping3 is designed to craft and send custom network packets. It is used to test firewall rules, intrusion detection systems (IDS/IPS), and overall network behavior. This tool is typically applied in advanced network testing and traffic simulation scenarios.

4. DNSRecon specializes in DNS enumeration. It retrieves DNS records and can attempt zone transfers to discover additional domain information. DNSRecon is mainly used to gather domain and subdomain details related to a target.


>Comparison of Maintaining access tools

1. PowerSploit is a PowerShell-based framework mainly used for post-exploitation tasks in Windows environments. It helps attackers or penetration testers perform privilege escalation, credential harvesting, and system control after gaining initial access.

2. Webshells are malicious scripts uploaded to a web server to provide remote access through a web browser. They are commonly used to maintain persistence and execute commands on compromised web servers.

3. Weevely is a stealthy PHP web shell tool that allows remote command execution and file management on a compromised server. It provides more structured control compared to basic webshells.

4. Dns2tcp is a tunneling tool that transmits TCP traffic over DNS queries. It is typically used to bypass firewall restrictions by hiding communication within DNS traffic.

5. Cryptcat is a modified version of Netcat that provides encrypted communication between systems. It is often used to create secure backdoors or transfer data stealthily.

**References**
[1] Repository & Wiki: * Tomes, T. (2026). Recon-ng: A full-featured Web Reconnaissance framework written in Python. GitHub. https://github.com/lanmaster53/recon-ng 
[2] Lyon, G. F. (2009). Nmap Network Scanning: The Official Nmap Project Guide to Network Discovery and Security Scanning. Insecure. https://nmap.org/book/
[3] FireCompass. (2024). Top 10 Tools for Reconnaissance. https://www.firecompass.com/wp-content/uploads/2024/02/FireCompass-Top-10-Tools-for-Reconnaissance.pdf
