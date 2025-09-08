# TryHackMe-ALL-Free-Room

Welcome to my repository documenting my journey through **all free TryHackMe rooms**, from beginner to advanced! This project tracks my progress in learning cybersecurity through hands-on challenges on [TryHackMe](https://tryhackme.com), a platform offering interactive labs to master skills like Linux, web exploitation, OSINT, and Capture The Flag (CTF) challenges. Whether you're a beginner or an experienced hacker, this repo aims to inspire and guide you through free, accessible cybersecurity training.

## About

This repository catalogs my solutions, writeups, and notes for TryHackMe’s free rooms, organized by skill level and topic. My goal is to complete every free room, starting with beginner-friendly ones and progressing to advanced challenges. Each room helps build practical skills in areas like:

- **Linux Fundamentals**: Navigating and manipulating Linux systems.
- **OSINT**: Gathering intelligence using tools like Google Dorking and `exiftool`.
- **Web Exploitation**: Exploiting vulnerabilities like SQL injection and LFI.
- **Privilege Escalation**: Gaining higher access on Linux and Windows systems.
- **CTFs**: Solving real-world hacking scenarios.

By sharing my journey, I aim to contribute to the cybersecurity community, inspire others to learn, and create a resource for beginners to follow. Feel free to explore, contribute, or use this as a guide for your own TryHackMe journey!

## Skills Showcased

Through completing TryHackMe’s free rooms, I’m developing and demonstrating skills critical for cybersecurity:

- **Reconnaissance**: Using OSINT tools (e.g., Google Dorking, `sherlock`, `exiftool`) to gather information.
- **Linux Proficiency**: Mastering commands like `ls`, `cd`, `grep`, `find`, and `nano` for system navigation and file manipulation.
- **Web Exploitation**: Identifying and exploiting vulnerabilities (e.g., file inclusion, command injection) using tools like `gobuster` and Burp Suite.
- **Enumeration**: Scanning networks and services with `nmap` to identify open ports and vulnerabilities.
- **Tool Usage**: Leveraging Kali Linux tools like `metasploit`, `hydra`, and `exiftool` for pentesting.
- **Problem-Solving**: Tackling CTF challenges with logical and creative approaches.

## Completed Rooms

Below is a progress tracker of free TryHackMe rooms I’ve completed, organized by skill level and topic. Writeups and notes are linked where available.

### Beginner (Green)
- **Platform Basics**
  - [Welcome](https://tryhackme.com/room/welcome): Learned TryHackMe’s interface and basics.
  - [OpenVPN](https://tryhackme.com/room/openvpn): Set up VPN access for TryHackMe labs.
- **Core Skills**
  - [Learn Linux](https://tryhackme.com/room/zthlinux): Mastered basic Linux commands (`ls`, `cat`, `grep`).
- **OSINT**
  - [OHsint](https://tryhackme.com/room/ohsint): Applied OSINT with `exiftool` and Google searches ([writeup](./writeups/OHsint-Writeup.md)).
  - [Google Dorking](https://tryhackme.com/room/googledorking): Learned advanced Google search operators (in progress).
- **CTFs**
  - [Basic Pentesting](https://tryhackme.com/room/basicpentestingjt): Practiced enumeration, brute-forcing, and privilege escalation.

### Intermediate (Yellow)
- (To be added as I progress)

### Advanced (Red)
- (To be added as I progress)

*Note*: Check the `writeups/` folder for detailed markdown files with steps, challenges faced, and lessons learned for each room.

## Setup Instructions

To follow along with my TryHackMe journey or replicate the challenges, set up your environment as follows:

### Prerequisites
- **TryHackMe Account**: Sign up for free at [tryhackme.com](https://tryhackme.com).
- **Kali Linux**: Download [Kali Linux](https://www.kali.org/get-kali/) (VM or live USB) for pre-installed pentesting tools.
  - Alternative: Use any Linux distro or Windows with tools installed manually.
- **OpenVPN**: Install to connect to TryHackMe’s networks.
  - On Kali: `sudo apt-get install openvpn`
- **Basic Tools**:
  - `exiftool`: For image metadata analysis (`sudo apt-get install exiftool`).
  - `sherlock`: For username searches (optional, install via `pip install sherlock-project`).
  - `nmap`, `gobuster`, `hydra`: Pre-installed on Kali for scanning and exploitation.
- **Browser**: Firefox or Chrome for accessing TryHackMe and performing OSINT tasks.

### Steps
1. **Join TryHackMe**: Create a free account and explore the “hacktivities” page (https://tryhackme.com/hacktivities) to find free rooms.
2. **Set Up VPN**: Complete the [OpenVPN](https://tryhackme.com/room/openvpn) room to download and configure the VPN file.
   - Run: `sudo openvpn your-vpn-file.ovpn`
3. **Access Rooms**: Start with beginner rooms listed above. Use Kali Linux for hands-on tasks.
4. **Document Progress**: Clone this repo and add your own writeups:
   ```bash
   git clone https://github.com/vatsayu/TryHackMe-ALL-Free-Room.git
   cd TryHackMe-ALL-Free-Room
   ```
   Create a writeup in the `writeups/` folder (e.g., `OHsint-Writeup.md`) and push to GitHub.

## How to Use This Repository
- **Browse Writeups**: Check the `writeups/` folder for detailed guides on completed rooms, including tools used and lessons learned.
- **Track Progress**: Follow the “Completed Rooms” section to see my journey and suggested order for beginners.
- **Contribute**: If you’ve completed other free rooms or have tips, submit a pull request with your writeup or suggestions!
  - Ensure rooms are free (check TryHackMe’s “Free” filter).
  - Add rooms to the relevant skill level in this README.
- **Images**: Screenshots (e.g., `exiftool` outputs) are in the `images/` folder for visual reference.

## Tips for Beginners
- **Start Simple**: Begin with green-level rooms (e.g., Welcome, Learn Linux) to build confidence.
- **Take Notes**: Document commands (e.g., `nmap -sV <IP>`) and findings for each room.
- **Use Hints**: TryHackMe’s in-room hints help when stuck, but avoid full walkthroughs to learn problem-solving.
- **Join the Community**: Ask questions on TryHackMe’s Discord or [r/tryhackme](https://www.reddit.com/r/tryhackme).
- **Practice Tools**: Familiarize yourself with Kali Linux tools through rooms like [Nmap](https://tryhackme.com/room/rpnmap) or [Metasploit](https://tryhackme.com/room/rpmetasploit).

## Current Progress
As of September 8, 2025, I’ve completed:
- **Welcome**, **OpenVPN**, **Learn Linux**, **Basic Pentesting**, and **OHsint**.
- Currently working on **Google Dorking** for Day 3.
- Next up: [Vulnversity](https://tryhackme.com/room/vulnversity) for web exploitation.

## Contributing
Want to help make this repo a go-to resource for TryHackMe learners? Contribute by:
- Adding writeups for free rooms I haven’t covered.
- Suggesting new free rooms (verify they’re free on TryHackMe).
- Improving this README with better formatting or tips.
Submit a pull request with your changes, and let’s build a stronger cybersecurity community together!

## Contact
- GitHub: [vatsayu](https://github.com/vatsayu)
- TryHackMe: [Your TryHackMe Profile URL, if public]
- For questions or suggestions, open an issue or reach out via TryHackMe’s Discord.

Happy hacking! 🚀 Let’s conquer all free TryHackMe rooms together!
