# [PROGRAM/BATCH]-[YOUR NAME]-[WEEK]-[MODULE]-FOOTPRINTING & NETWORK SCANNING PHASES
###
## 👤 Lab Information
 
| **Field** | **Details** |
|---|---|
| **Pentester Name**<br>*(Cybersecurity Professional)* | **[YOUR FULL NAME]** |
| **Program/Batch** | [PROGRAM NAME - BATCH NUMBER] |
| **Date** | [DD MONTH YYYY] |
| **Modules Completed** | [MODULE CODE] ([Module Description])<br>[MODULE CODE] ([Module Description]) |
| **Client/Target** | 1. [Target Organization] (secured written permission already)<br>2. My own local LAN Network |
| **Permission secured from client?** | **Yes / No** |
| **Phases Covered** | **Phase 1:** Reconnaissance & Footprinting<br>**Phase 2:** Scanning & Network Discovery |
###
 
## 1. Introduction
This report documents [NUMBER] cybersecurity activities completed as part of my ongoing internship/training at [PROGRAM NAME]. The first module focuses on **domain footprinting using multiple Kali Linux tools**, while the second covers **local network discovery and scanning with [TOOL, e.g. Zenmap]**.
Together, these exercises demonstrate the progression from **collecting publicly available information about a target to identifying and mapping active hosts within a network**.
All activities were performed using **[Operating System(s) used]**. Each section documents the command or procedure used, the observed output, supporting screenshot evidence, and a brief explanation of the security relevance of each finding.
 
## 2. 🛠️ Tools Used
 
The table below lists the tools used in this report and their respective purposes.
 
| **Tool** | **Purpose** |
|---|---|
| **[OS name(s)]** | Operating systems used for reconnaissance and network-scanning activities |
| **WHOIS** | Retrieve domain registration information such as ownership details, registration dates, and name servers |
| **WhatWeb** | Identify web technologies, servers, CMS platforms, plugins, and related information |
| **nslookup** | Resolve domain names to their corresponding IP addresses using DNS |
| **curl -I** | Retrieve and examine HTTP response headers from the target website |
| **WAFW00F** | Identify whether a Web Application Firewall (WAF) is protecting the website |
| **dnsrecon** | Enumerate DNS records including NS, MX, SPF, TXT, and SRV records |
| **[Scanning tool, e.g. Zenmap/Nmap]** | Discover live hosts, open ports, and network information on the local subnet |
| **[Windows CMD / terminal]** | Identify local IP address and MAC address information |
 
####
# 3. Activities Performed
 
## 3.1 Footprinting & Reconnaissance
 
During the reconnaissance stage, I conducted a passive assessment of the **[target-domain.com]** domain using [NUMBER] Kali Linux tools: **WHOIS, WhatWeb, Nslookup, cURL, Wafw00f, and DNSRecon**. Each tool was used to examine a different aspect of the target's publicly accessible infrastructure.
 
###
# WHOIS
**WHOIS** is used to gather publicly available domain registration information and determine the name servers associated with the domain.
 
*[Describe what you found — registrar, registration date, name servers, etc.]*
 
<!-- Insert screenshot(s) here -->
<!-- ![WHOIS output](path-or-link-to-image) -->
 
###
# WHATWEB
Next, I used **WhatWeb** to fingerprint the technologies powering the website.
 
*[Describe results — CMS, plugin versions, server software, etc.]*
 
<!-- Insert screenshot here -->
 
###
# NSLOOKUP
I then performed a DNS lookup with **Nslookup** to determine the IP address associated with the domain.
 
*[State the resolved IP address]*
 
<!-- Insert screenshot here -->
 
###
# CURL -I
I then used **cURL** with the `-I` option to examine the website's HTTP response headers.
 
*[Describe headers/endpoints revealed, e.g. REST API paths, server banner]*
 
<!-- Insert screenshot here -->
 
###
# WAFW00F
Next, I ran **Wafw00f** to identify whether a Web Application Firewall (WAF) was deployed in front of the website.
 
*[State WAF detected, or "no WAF detected"]*
 
<!-- Insert screenshot here -->
 
###
# DNSRECON
Finally, I used **DNSRecon** to gather available DNS information associated with the domain.
 
*[Summarize NS, MX, SPF/TXT, SRV records found]*
 
<!-- Insert screenshot here -->
 
These findings provided additional visibility into the target's **web-server configuration, security controls, and DNS infrastructure**, contributing to the overall reconnaissance profile.
 
###
## 3.2 Network Scanning with [Zenmap/Nmap]
 
The second practical activity focused on **network discovery and host identification** within my local network. The objective was to determine the local IP address and subnet, identify active devices, obtain their IP and MAC addresses, and visualize the discovered hosts.
 
I began by running **[ipconfig / ifconfig]** to obtain the computer's local IP address and determine the applicable LAN subnet.
 
<!-- Insert screenshot here -->
 
I then configured [tool] with the identified subnet **[e.g. 192.168.x.x]** and performed a **Ping Scan** to detect devices that were actively responding on the network. Command used:
 
```
nmap -sn -PR [subnet]/24
```
 
The practical exercise identified the following live hosts:
 
- `[IP address 1]`
- `[IP address 2]`
- `[IP address 3]`
The scan also returned corresponding **MAC address information** for the discovered devices.
 
<!-- Insert screenshot here -->
 
After completing the host discovery scan, I [visualized the topology / exported results], as required by the practical exercise.
 
<!-- Insert screenshot here -->
 
###
 
## 4. Risk Analysis / Impact
 
The reconnaissance and network-scanning exercises produced several findings that may have security implications. The observations below summarize the identified exposures and their potential impact.
 
| # | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | **[Finding]** | [What tool/observation revealed this] | [Why it matters] | 🟡 **Low** / 🟠 **Medium** / 🔴 **High** |
| 2 | **[Finding]** | [Evidence] | [Impact] | [Risk Level] |
| 3 | **[Finding]** | [Evidence] | [Impact] | [Risk Level] |
 
### Risk Level Classification
 
- 🟡 **Low:** Limited exposure with relatively low immediate security impact.
- 🟠 **Medium:** Information that could contribute to further reconnaissance or increase exposure.
- 🔴 **High:** Findings that could present a significant security risk and require prompt attention.
###
 
## 5. Security Recommendations
 
- Keep [CMS/software] regularly updated.
- Minimize unnecessary technical information exposed through HTTP headers and public endpoints.
- Review and secure DNS records and remove outdated or unnecessary entries.
- Maintain and regularly update WAF security rules and configurations.
- Monitor the local network for unknown or unauthorized devices.
- Conduct periodic vulnerability assessments and network security scans.
- Apply strong access controls to administrative and sensitive services.
- Enable security logging and monitor for suspicious network activity.
- Protect sensitive configuration and system information from public exposure.
- Document findings and verify that identified security issues are properly addressed.
## 6. Conclusion
 
*[Write a summary paragraph or two covering: what phases were completed, what tools were used, key takeaways from the footprinting phase, key takeaways from the scanning phase, why authorized/controlled testing matters, and what skills were reinforced.]*
 
*[Optionally add a closing paragraph on how this exercise sets up the next stage of the engagement — e.g. service enumeration, vulnerability identification, exploitation testing.]*
 
###
**👤 Author**
 
**[ADEWUYI GODWIN OLUWAPELUMI]**
[CYBERSECURITY INTERN] | [Batch/Program ID]
LinkedIn: [www.linkedin.com/in/godwin-adewuyi-58244236b]
 
---
 
**📌 Project Information**
 
**Program Name:** [Program Name] | **Week:** [Week Number] | **Project:** [Project Title] | **Repository:** GitHub
