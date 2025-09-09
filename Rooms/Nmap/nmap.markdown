# TryHackMe: Nmap Writeup

**Room**: [Nmap](https://tryhackme.com/room/nmap01)  
**Difficulty**: Beginner  
**Author**: [r3Tro](https://tryhackme.com/p/r3Tro)  
**Date**: September 10, 2025  

## Overview
The **Nmap** room on TryHackMe introduces Nmap (Network Mapper), a powerful open-source tool for network reconnaissance and security auditing. This beginner-friendly room teaches how to perform basic network scans, detect service versions, identify operating systems, and target specific ports on a machine. It’s a foundational step for penetration testing, as scanning is often the first phase in identifying vulnerabilities.

## Objectives
- Understand Nmap’s purpose and basic commands.
- Perform scans to identify open ports, services, and operating systems.
- Learn to save and interpret scan results for further analysis.

## Tools Used
- **Nmap**: Installed on TryHackMe’s AttackBox (browser-based Kali Linux).
- **TryHackMe VPN**: Connected via OpenVPN to access the target machine.
- **Terminal**: For running Nmap commands and saving outputs.

## Methodology
1. **Task 1: Introduction to Nmap**  
   - Read about Nmap’s role in network scanning and its importance in pentesting.  
   - Answered a question about Nmap’s full name: “Network Mapper.”  

2. **Task 2: Basic Scanning**  
   - Deployed the room’s virtual machine to get the target IP (e.g., 10.10.x.x).  
   - Ran a basic scan using the command:  
     ```bash
     nmap <target_ip>
     ```  
   - This listed open ports (e.g., 22/tcp open ssh, 80/tcp open http).  
   - Answered a question about the number of open ports by counting them in the output (e.g., 3 ports).  
   - Saved the scan output for reference:  
     ```bash
     nmap <target_ip> -oN nmap_basic.txt
     ```

3. **Task 3: Service Version Detection**  
   - Used the `-sV` flag to identify service versions:  
     ```bash
     nmap -sV <target_ip>
     ```  
   - The output showed details like “OpenSSH 7.6p1” or “Apache httpd 2.4.7.”  
   - Answered a question about the version of a specific service (e.g., SSH) by checking the output.  

4. **Task 4: Aggressive Scanning**  
   - Performed a detailed scan using the `-A` flag:  
     ```bash
     nmap -A <target_ip>
     ```  
   - This provided OS detection, script scanning, and service versions.  
   - Answered a question about the target’s operating system (e.g., “Linux 3.x”) by checking the “OS details” section.  
   - Noted that `-A` scans are slower but more comprehensive.  

5. **Task 5: Specific Port Scanning**  
   - Scanned specific ports (e.g., HTTP and HTTPS) using:  
     ```bash
     nmap -p 80,443 <target_ip>
     ```  
   - Checked if ports were open (e.g., “80/tcp open http” or “443/tcp closed”).  
   - Answered a question about the status of a specific port (e.g., “Is port 443 open?”).  
   - Used the `-Pn` flag if the host appeared down:  
     ```bash
     nmap -Pn -p 80,443 <target_ip>
     ```

## Key Learnings
- **Nmap Commands**: Mastered basic commands like `nmap <target>`, `-sV` for service versions, `-A` for aggressive scans, and `-p` for specific ports.
- **Scan Interpretation**: Learned to read Nmap output to identify open ports, services, and OS details.
- **Practical Application**: Understood how Nmap fits into the pentesting workflow, especially for reconnaissance in rooms like **Vulnversity**.
- **Troubleshooting**: Used `-Pn` to bypass host discovery issues and saved outputs for analysis.

## Screenshots
*(Add screenshot of Nmap scan output)*  
To add: Capture the terminal output of `nmap -A <target_ip>` and save it as `nmap_scan.png`. Upload to your GitHub repo in the same folder as this writeup.

## Challenges Faced
- **Host Down Errors**: Initially, some scans failed with “host seems down.” Resolved by using the `-Pn` flag to skip host discovery.  
- **VPN Issues**: Ensured TryHackMe VPN was connected via OpenVPN setup to access the target.  
- **Slow Scans**: Noticed that `-A` scans took longer; adjusted by running faster scans first to confirm open ports.

## Next Steps
- Apply Nmap skills in practical pentesting rooms like **Vulnversity** or **Blue**.  
- Explore advanced Nmap features, such as script scanning (`--script`), in rooms like **Nmap Live Host Discovery**.  
- Practice saving and analyzing scan results for real-world scenarios.

## Notes
- Always connect to TryHackMe’s VPN before scanning to ensure access to the target machine.  
- Refer to `man nmap` or `nmap --help` in the terminal for additional command options.  
- Join TryHackMe’s Discord or r/tryhackme for community support if stuck.