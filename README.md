## Hi there 👋
#disclaimer(This project is for educational purposes only. All testing was performed in a controlled environment or on authorized targets.)

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
