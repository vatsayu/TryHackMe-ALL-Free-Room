# Linux Fundamentals Part 1 Writeup - TryHackMe

## Overview
The **Linux Fundamentals Part 1** room on TryHackMe (https://tryhackme.com/room/linuxfundamentalspart1) is a beginner-friendly walkthrough that introduces essential Linux commands and file system navigation. This writeup outlines the methodology to complete the room, focusing on commands like `echo`, `whoami`, `ls`, `cd`, `grep`, and `find`, without revealing specific answers. These skills are foundational for CTF challenges and pentesting.

## Tools Used
- **Kali Linux**: For accessing the TryHackMe virtual machine via SSH or in-browser terminal.
- **Basic Commands**: `echo`, `whoami`, `ls`, `cd`, `cat`, `grep`, `find`, `wc`.

## Steps to Solve

### Step 1: Deploy the Machine
- **Task**: Start the Linux virtual machine provided by TryHackMe.
- **Approach**:
  - Click “Start Machine” to deploy the Ubuntu-based VM.
  - Note the IP address and use SSH (`ssh tryhackme@<IP>`) or the in-browser terminal.
- **Tips**:
  - Ensure you’re connected to TryHackMe’s VPN (from the OpenVPN room).
  - If SSH fails, verify the IP and port or use the browser terminal.

### Step 2: Learn Basic Commands
- **Task**: Understand and practice commands like `echo`, `whoami`, `ls`, and `cd`.
- **Approach**:
  - Use `echo` to display text (e.g., `echo TryHackMe`).
  - Run `whoami` to check the current user (e.g., `tryhackme`).
  - Use `ls` to list files and `cd` to navigate directories (e.g., `cd /home/tryhackme`).
- **Tips**:
  - Try `ls -la` to see hidden files.
  - Use `man <command>` (e.g., `man ls`) for command details.

### Step 3: File System Tasks
- **Task**: Answer questions involving file navigation and content reading.
- **Approach**:
  - Navigate to specific directories using `cd` (e.g., `cd folder4`).
  - Read files with `cat filename` or `less filename`.
  - Find files with `find / -name filename` or `locate filename`.
- **Tips**:
  - For path questions, use `pwd` to get the current directory.
  - If a file is hard to find, try `find / -name "*.txt"` for text files.

### Step 4: Search for Flags
- **Task**: Locate flags (e.g., prefixed with “THM”) in files.
- **Approach**:
  - Use `grep` to search file contents: `grep "THM" filename`.
  - For recursive searches: `grep -r "THM" /home/tryhackme`.
  - Count lines with `wc -l filename` if asked.
- **Tips**:
  - Check TryHackMe hints if no flags are found.
  - Be case-sensitive when submitting flags.

## Example Image
Below is a placeholder for a screenshot of a command output (e.g., `ls -la` or `grep` result). To include it in your GitHub repo:
1. Take a screenshot on Kali Linux: `scrot linux-fundamentals.png`.
2. Upload to your repo’s `images/` folder.
3. Update the markdown:  
   ```markdown
   ![Command Output](images/linux-fundamentals.png)
   ```

*Placeholder*:  
![Command Output](images/linux-fundamentals.png)

## Challenges Faced
- **Navigation Errors**: Mistyped `cd` commands; double-check directory names with `ls`.
- **Permission Denied**: Some files may require `sudo` or specific paths; verify the question’s context.
- **Finding Flags**: If `grep` finds nothing, try broader searches with `find` or check hints.

## Lessons Learned
- **Linux Basics**: Commands like `ls`, `cd`, and `grep` are essential for CTFs.
- **Systematic Approach**: Enumerating files and directories methodically saves time.
- **Tool Mastery**: Practicing commands in Kali Linux builds confidence for future rooms.

## Next Steps
- Continue with [Linux Fundamentals Part 2](https://tryhackme.com/room/linuxfundamentalspart2) if free, or try [Vulnversity](https://tryhackme.com/room/vulnversity) for web exploitation.
- Apply Linux skills in CTFs like [Basic Pentesting](https://tryhackme.com/room/basicpentestingjt).