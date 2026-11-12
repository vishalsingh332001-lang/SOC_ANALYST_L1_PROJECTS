# SOC_ANALYST_L1_PROJECTS
# **📧 SOC L1 Analyst Portfolio: Phishing Email Analysis & Alert Triage**

**This repository contains the practical cybersecurity artifacts, playbooks, and ticketing documentation I completed to demonstrate SOC Tier 1 alert triage, email analysis, and incident escalation methodologies.**

## **📂 Projects & Investigations**

### **Email Phishing Investigation**
* **Focus:** **Spear-phishing analysis**, **header extraction**, and **payload detonation**.
* **Scenario:** An end-user reported a suspicious email titled **"URGENT: Q3 Invoice Discrepancy."**
* **Actions Taken:** 
  * Analyzed **raw email headers** (`Received`, `Return-Path`) to identify **domain spoofing** and **SPF/DMARC failures**.
  * Safely detonated the attached **`.xlsm` payload** in a malware sandbox to observe **macro execution** and **process creation**.
  * Extracted critical **Indicators of Compromise (IoCs)** and mapped the attack to **MITRE ATT&CK (T1566.001 - Spearphishing Attachment)**.
  * Authored a professional **escalation ticket** recommending containment actions (**IP/Domain blocking**).

## **🔍 Threat Intelligence & Artifacts**
The `/Artifacts` and `/Incident_Tickets` folders in this repository contain:
* **Raw Email Headers:** Highlighting the true originating IP (**`103.14.22.89`**).
* **Sandbox Process Trees:** Documenting a malicious **Excel macro** spawning **PowerShell** to download a secondary payload.
* **Threat Intelligence Reports:** **VirusTotal API** and **OSINT data** confirming the malicious reputation of the sender IP and payload URL.
* **Triage Ticket (INC-84729):** A mock **ServiceNow/Jira ticket** detailing the investigation findings and escalation handoff to **Tier 2**.

## **🛠️ Tools Used**
* **Email Analysis:** **MXToolbox**, manual email header parsing
* **Malware Sandboxing:** **Any.Run**
* **Threat Intelligence / OSINT:** **VirusTotal**, **AbuseIPDB**, **URLScan.io**
* **Workflow:** **Markdown**, **Standard Operating Procedures (SOPs)**, **Incident Ticketing**

## **📈 What I Demonstrated**
* **Investigating and triaging** suspicious user-reported emails within defined SLAs.
* **Extracting and analyzing** raw email headers to trace attacker infrastructure.
* **Safely detonating malicious attachments** in isolated environments (Sandboxes) to extract **file hashes** and **network callbacks**.
* **Checking IPs, URLs, and domains** using industry-standard threat intelligence tools.
* **Following structured SOC playbooks** for consistent incident handling.
* **Writing clear, actionable investigation reports** and escalation tickets.

---

## **📬 About Me & Contact**
* **Connect with me on LinkedIn:** **[www.linkedin.com/in/vishal-singh-b6aa32218]**
* Contact No: 6302334628
* **Location:** **Hyderabad, Telangana**
