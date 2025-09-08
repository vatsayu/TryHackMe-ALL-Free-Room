# OHsint Writeup - TryHackMe

## Overview
The **OHsint** room on TryHackMe is a beginner-friendly Open-Source Intelligence (OSINT) challenge focused on gathering information from online sources. This writeup documents the methodology to solve the room, emphasizing OSINT techniques like image metadata analysis and social media reconnaissance, without spoiling specific answers. The room involves analyzing clues (e.g., an image or username) to answer questions and find flags.

## Tools Used
- **Kali Linux**: For running `exiftool` and other command-line tools.
- **Web Browser**: For Google searches and checking platforms like Twitter/X.
- **exiftool**: To extract metadata from images.
- **Sherlock (Optional)**: For searching usernames across platforms.

## Steps to Solve

### Step 1: Understand the Objective
- **Task**: The room provides an initial clue, typically an image or username, and asks questions requiring OSINT to find details like locations, usernames, or flags.
- **Approach**: Read all tasks carefully to identify the starting point (e.g., an image file named `sherlock.jpg` or a username). Note any specific platforms or tools mentioned.

### Step 2: Analyze the Provided Image
- **Task**: Download the image provided in the room (e.g., via TryHackMe’s interface).
- **Approach**:
  - Save the image to your Kali Linux machine (e.g., `/home/user/ohsint.jpg`).
  - Use `exiftool` to extract metadata:  
    ```bash
    exiftool ohsint.jpg
    ```
  - Look for useful metadata like GPS coordinates, author names, or comments that could lead to answers.
  - If GPS coordinates are found, use an online map (e.g., Google Maps) to pinpoint the location.
- **Tips**:
  - Install `exiftool` if not already on Kali: `sudo apt-get install exiftool`.
  - If no metadata is found, check the image visually for clues (e.g., text, landmarks).
  - Example output might include fields like `GPS Latitude` or `Description`.

### Step 3: Search for Usernames or Clues
- **Task**: If the room provides a username or text clue, search for it across online platforms.
- **Approach**:
  - Use Google with operators (learned from the **Google Dorking** room):  
    ```text
    inurl:username site:twitter.com
    ```
  - Check platforms like Twitter/X, GitHub, or Instagram directly for the username.
  - Optionally, use `sherlock` to automate username searches:  
    ```bash
    sherlock username
    ```
  - Analyze profiles for details like location, bio, or linked accounts that answer questions.
- **Tips**:
  - Look for posts or bios mentioning locations, emails, or other clues.
  - Cross-reference findings (e.g., a Twitter/X bio linking to a blog) to confirm answers.

### Step 4: Answer Questions
- **Task**: Submit answers to TryHackMe’s questions based on your findings.
- **Approach**:
  - For location-based questions: Use GPS coordinates from `exiftool` or profile details.
  - For flag-based questions: Check metadata, profile posts, or linked sites for hidden flags.
  - For personal details (e.g., email, name): Search social media or use Google Dorking techniques.
- **Tips**:
  - Be thorough: Re-check clues if an answer is rejected.
  - Use TryHackMe’s hints if stuck, but avoid full walkthroughs to maximize learning.

### Step 5: Document Findings
- **Task**: Keep notes for future reference or writeups like this one.
- **Approach**:
  - Log commands used (e.g., `exiftool ohsint.jpg > metadata.txt`).
  - Save screenshots of key findings (e.g., `exiftool` output, Google search results).
  - Organize answers in a text file to track progress.

## Example Image
Below is a placeholder for a screenshot of `exiftool` output or a Google search relevant to the room. To include it in your GitHub repo:
1. Take a screenshot of your `exiftool` output or a Google search result (e.g., using `scrot` on Kali: `scrot screenshot.png`).
2. Upload the image to your repo (e.g., in an `images/` folder).
3. Update the markdown with the correct path:  
   ```markdown
   ![exiftool Output](images/exiftool-ohsint.png)
   ```

*Placeholder*:  
![exiftool Output](images/exiftool-ohsint.png)

## Challenges Faced
- **No Metadata in Image**: If `exiftool` returns no useful data, focus on visual clues or search for usernames found in the image.
- **Platform Overload**: If a username appears on multiple platforms, prioritize Twitter/X or GitHub, as they often hold key details.
- **Wrong Answers**: Double-check spelling or format (e.g., flags are case-sensitive).

## Lessons Learned
- **OSINT Power**: Combining tools like `exiftool` and Google Dorking can uncover hidden information quickly.
- **Attention to Detail**: Small clues (e.g., a bio’s mention of a city) can lead to answers.
- **Tool Familiarity**: Practicing `exiftool` and search operators builds confidence for future CTFs.

## Next Steps
- Try another OSINT room like **Shodan.io** to learn network discovery.
- Move to CTF rooms like **Vulnversity** to apply Linux and pentesting skills from previous rooms.