---

layout: col-sidebar
title: OWASP Port and Service Information
tags: nmap script, scan sites,exploit detection, fuzzing, service enumeration
level: 2
type: 
pitch: Nmap Script to extend the functionality of scanning by providing more information about ports,services,exploits and fuzzing.

---
## Description
This project is basically working around a custom nmap script. This will be helpful for initial enumeration phases when the attacker needs more information about already available information about open ports,services,exploits and other details. The source of the information will be a readily available data file which will help users to do initial enumeration much quickly.

### Example: 
1. Nmap detects port 80 running Apache Server
2. Script gets information about the port
3. It checks the apache version and tries to find vulnerabilities available on internet(including but not limited to ExploitDb)
4. It loads the page and checks it contents to detect what stack the website is running and what CMS is it using,
5. It will use the  new found information and execute Step 3
6. If user selected fuzzing options, such as directory fuzzing or subdomain fuzzing, it will automatically launch fuzzers
7. Similarly, it will try to enumerate FTP port, SMTP port and other ports found on basis of enumeration and tools available. Data source will be the central Data file.
7. For any new findings, it will run Steps 3-5 (depending on the argument set by the user)

## Project Roadmap
1. The project will start with creation of a small and central database.
2. Script creation for Port Information
3. Exploit detection based on enumeration
4. Service Detection
5. Service Detailed Enumeration
6. Fuzzers
