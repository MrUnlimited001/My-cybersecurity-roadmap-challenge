# 🖧 Week 5: Scanning & Enumeration 
Welcome to Week 2 of my 90-Day Cybersecurity Roadmap Challenge 🚀

This week focuses on the fundamentals of network scanning and host/service enumeration using Nmap and hands-on TryHackMe labs. I practiced service enumeration techniques (FTP, SSH, SMB), explored brute-force and enumeration strategies, and researched OSINT methods to improve reconnaissance. The week ends with this GitHub-ready recap.

## 📆 Daily Breakdown

---

### 📅 Day 28
Goal: Learn Nmap basics (scanning)
-	Read tutorials and ran local Nmap scans against lab VMs.
-	Learned scan types: 
1.	TCP SYN (-sS) 
2.	TCP connect (-sT)
3.	UDP (-sU).
-	Practiced useful flags: 
1.	-p (port selection)
2.	 -A (aggressive: OS/service detection, version, script)
3.	-sV (service/version detection)
4.	 -O (OS detection)
5.	-Pn (no host discovery)
6.	-T4 (timing template)
7.	 -oA (output in all formats).

---

### 📅 Day 29:
Goal: Do TryHackMe Nmap room
-	Completed TryHackMe Nmap room exercises to consolidate command usage and interpretation.
-	Improved speed and confidence with common Nmap workflows.
-	Practiced reading Nmap output: identifying open ports, services, versions, and likely attack vectors.
-	Learned to combine Nmap NSE scripts for targeted checks (e.g., --script vuln, --script safe when appropriate).

---

### 📅 Day 30:
Goal:  Do TryHackMe: Basic Pentesting room
-	Applied Nmap scanning in a basic pentesting workflow (recon → scan → enumerate → exploit path planning).
-	Built a repeatable workflow: recon (OSINT + discovery) → port scan (Nmap) → service enumeration → exploit research.
-	Documented scan results for downstream use in report writing.

---

### 📅 Day 31:
Goal: Learn Service enumeration (FTP, SSH, SMB)
-	Hands-on enumeration of common services; practiced passive and active techniques.
-	Quick notes & commands:
-	FTP (File transfer protocol)
1.	Check anonymous login: ftp 10.10.0.5 or with nmap script: Nmap –script ftp-anon -p21 10.10.0.5
2.	Use ftp, nc, or curl to interact; list directories and look for interesting files (credentials, configs).
-	SSH (Secure remote Shell)
1.	Enumerate SSH banner and versions via Nmap/join with ssh -v for manual probing: Nmap -sV -p22 –script ssh-hostkey 10.10.0.5
2.	Ssh -v user@10.10.0.5
3.	For bruteforce (lab only), tools like hydra or medusa can be used with appropriate wordlists.
-	SMB
-	Enumerate shares and users with smbclient, smbmap, and Nmap scripts:
1.	Smbclient -L \\\\10.10.0.5 -N
2.	Smbmap -H 10.10.0.5
3.	Nmap –script smb-enum-shares,smb-enum-users -p445 10.10.0.5
-	Look for writable shares, default creds, and exposed config/backups.
-	Safety note: Only use brute-force tools and intrusive scripts within lab environments or with explicit authorization.

---

### 📅 Day 32:
Goal:  Do TryHackMe: Enumeration and Bruteforce room.
-	Completed the lab focusing on enumeration, credential harvesting, and controlled brute-force attempts.
-	Practiced correlating service banners and versions to known vulnerabilities.
-	Used wordlists and credential reuse strategies to pivot to additional services.
-	Emphasized documentation of every step and evidence collection (screenshots, logs, saved Nmap outputs).

---

### 📅 Day 33:
-	Goal: Research OSINT (for reconnaissance)
-	Researched OSINT techniques to enhance the reconnaissance phase prior to active scanning.
-	Highlights:
1.	Value of passive information gathering before noisy scans: domain WHOIS, DNS records, public subdomains, employee LinkedIn, public code repos, paste sites, and metadata in public files.
2.	Complementing technical scans with OSINT reduces unnecessary noise and helps craft targeted scans.
3.	Learned legal and ethical rules for OSINT reconnaissance.
4.	Learned step-by-step practical workflow and common pitfalls. 
-	Core tools and sources:
1.	Search engines and advanced queries: Google, Bing, Google dorks. 
2.	Web archives: Wayback Machine (archive.org)
3.	Domain / DNS / WHOIS: whois, dig, DNS history services. 
4.	Device and port scanners (discovery): shodan, censys.
5.	Automation Frameworks: Spiderfoot, Recon-ng.
6.	People / Social Footprint: LinkedIn, X, Facebook,  Instagram,  Sherlock,  GHunt.
7.	Metadata & Images: ExifTool, Google lens, Yandex reverse image.
8.	Email / breach search: HaveIBeenPwned, IntelX.
9.	Visualization: Maltego (graph analysis).

---

### 📅 Day 34:
Goal: Write scanning recap in GitHub
- Wrote a detailed recap summarizing all key learnings.
- Highlighted tools, commands, and key takeaways.

---

## 🛠 Tools Used
- **Linux Firefox Browser**
- **TryHackme Website**
-**Linux terminal**
-**TryHackme OpenVPN**
- **LinkedIn**

---

## 📌 Hands-on Practice
- ✅ Applied Nmap scanning on my Linux VM terminal as well as TryHackMe Nmap and pentesting room 
- ✅ Did OSINT reconnaissance using Google, Domain services and LinkedIn.
- ✅ Strengthened understanding of scanning and enumeration  with TryHackMe machines and tasks.

---

## ✅️ Summary Of What I Learned
-	Learned the core functions of Nmap: host discovery, port scanning, and service detection.
-	Practiced essential flags like -sS, -sV, -A, and saving results using -oA.
-	Applied Nmap commands in a guided TryHackMe lab environment.
-	Improved understanding of scan interpretation and NSE script usage.
-	Combined scanning, enumeration, and basic exploitation workflows.
-	Understood how Nmap fits into a structured pentesting process.
-	Practiced enumerating key services using tools like ftp, smbclient, and Nmap scripts.
-	Learned to detect anonymous FTP access, SSH versions, and SMB shares.
-	Performed targeted enumeration and controlled brute-force attempts.
-	Strengthened skills in identifying weak credentials and service misconfigurations.
-	Explored passive reconnaissance techniques such as WHOIS, DNS lookups, and subdomain discovery.
-	Learned the importance of gathering information before active scanning.
-	Summarized weekly learning into a GitHub recap document.

---

## 🎯 Goals For Next Week 
-	Learn about exploits, CVEs, Metasploit. 
-	Do TryHackMe: “Metasploit Intro”. 
-	Do TryHackMe: “Vulnversity”. 
-	Do TryHackMe: “Blue” (Windows exploitation). 
-	 Write notes on exploitation flow. 
-	Complete Hack The Box Starting Point machines (1 per day).




