# Google Dorking Writeup - TryHackMe

## Overview
The **Google Dorking** room on TryHackMe (https://tryhackme.com/room/googledorking) is a beginner-friendly Open-Source Intelligence (OSINT) walkthrough that teaches advanced Google search techniques using operators like `site:`, `inurl:`, and `filetype:`. This writeup documents the methodology to complete the room, focusing on crafting precise queries to find specific information, without revealing exact answers. Completed by [r3Tro](https://tryhackme.com/p/r3Tro) on September 8, 2025.

## Tools Used
- **Web Browser**: Firefox or Chrome for performing Google searches.
- **Text Editor**: Optional for noting queries (e.g., `nano` on Kali Linux).

## Steps to Solve

### Step 1: Understand Google Search Operators
- **Task**: Learn the purpose of operators like `site:`, `inurl:`, `filetype:`, and quotes (`"phrase"`).
- **Approach**:
  - Review the room’s tasks to grasp each operator:
    - `site:example.com`: Limits results to a specific domain.
    - `inurl:login`: Finds URLs containing “login.”
    - `filetype:pdf`: Returns specific file types.
    - `"exact phrase"`: Matches exact text.
  - Experiment with combining operators (e.g., `site:*.edu filetype:pdf`) in Google.
- **Tips**:
  - Test queries to see how results narrow with each operator.
  - Keep a log of effective queries for reference.

### Step 2: Apply Operators to Tasks
- **Task**: Answer questions by crafting Google queries to locate files, pages, or specific data.
- **Approach**:
  - Identify the question’s target (e.g., a PDF on a domain).
  - Build a query using relevant operators (e.g., `site:target.com filetype:txt`).
  - Browse search results to find the correct file or page, then extract the required information.
- **Tips**:
  - Use quotes for multi-word phrases (e.g., `"confidential report"`).
  - Exclude irrelevant results with `-` (e.g., `-inurl:signup`).
  - Verify the result matches the task before submitting.

### Step 3: Analyze Sitemap and Robots.txt
- **Task**: Explore sitemap and robots.txt files to gather additional clues.
- **Approach**:
  - Use Google to search for sitemap.xml (e.g., `site:target.com sitemap.xml`) or robots.txt (e.g., `site:target.com robots.txt`).
  - Download or view the files in the browser to identify indexed pages or disallowed directories.
  - Note any paths or keywords that could lead to answers.
- **Tips**:
  - Look for patterns in sitemap.xml (e.g., `/page1`, `/page2`) or disallowed entries in robots.txt (e.g., `/admin/`).
  - Combine findings with other operators (e.g., `site:target.com inurl:/admin/`).

### Step 4: Document Findings
- **Task**: Record successful queries and observations for future reference.
- **Approach**:
  - Save queries in a text file (e.g., `echo "site:target.com filetype:pdf" >> queries.txt`).
  - Take screenshots of key results, including sitemap and robots.txt files.
- **Tips**:
  - Use TryHackMe hints if a query fails to yield results.
  - Organize notes by task for easy review.

## Example Images
Below are placeholders for screenshots of the sitemap and robots.txt files. To include them in your GitHub repo:
1. Take screenshots of the sitemap.xml and robots.txt files you found during the room (e.g., `scrot sitemap.png` and `scrot robots.txt.png` on Kali Linux).
2. Upload them to your repo’s `images/` folder.
3. Update the markdown with the correct paths:  
   ```markdown
   ![Sitemap Example](images/sitemap.png)
   ![Robots.txt Example](images/robots.txt.png)
   ```

*Placeholders*:  
![Sitemap Example](images/sitemap.png)  
![Robots.txt Example](images/robots.txt.png)

## Challenges Faced
- **Broad Search Results**: Initial queries returned too many hits; refined with additional operators.
- **File Not Found**: Some files required exact domain matches; double-checked spelling.
- **robots.txt Access**: Needed to adjust queries to locate the file on the target domain.

## Lessons Learned
- **Operator Precision**: Combining `site:` and `filetype:` targets searches effectively.
- **OSINT Value**: Sitemap and robots.txt files reveal hidden or indexed content.
- **Practice Benefit**: Experimenting with queries builds intuition for reconnaissance.

## Next Steps
- Apply OSINT skills in rooms like [OHsint](https://tryhackme.com/room/ohsint) or [Shodan.io](https://tryhackme.com/room/shodan).
- Move to CTF rooms like [Vulnversity](https://tryhackme.com/room/vulnversity) for exploitation practice.