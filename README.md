
# 📧 SOC L1 Analyst Portfolio: Phishing Email Analysis & Alert Triage

Welcome to my portfolio! I am a cybersecurity professional based in Hyderabad with three years of frontline experience in SOC Tier 1 operations. 

During my time as a SOC L1 Analyst and Nesting SME, I learned that cybersecurity is rarely about relying solely on automated dashboard alerts—it is about digging into the raw data to uncover the truth. This repository showcases my daily methodology for investigating, triaging, and escalating suspicious threats before they compromise a network.

## 🕵️‍♂️ The Investigation: Spear-Phishing Triage

**The Scenario:** 
A panicked end-user reported a highly suspicious email with the subject line: **"URGENT: Q3 Invoice Discrepancy."** The email pressured the user to open an attached Excel file or face immediate service suspension. 

**The Analyst Workflow:**
Instead of taking the email at face value, I treated it as a live crime scene and followed standard SOC playbooks to tear the attack apart safely.

1. **Unmasking the Sender (Header Analysis):** 
   Attackers often spoof trusted domains, but the raw data never lies. I extracted the `.eml` file and manually parsed the `Received` and `Return-Path` headers. I discovered that while the email claimed to be from a known vendor, the true originating IP was `103.14.22.89`. Both SPF and DMARC checks failed, confirming it was a sophisticated spoofing attempt.
   
2. **Disarming the Payload (Malware Sandboxing):** 
   Knowing the attachment (`Invoice_Q3_Updated.xlsm`) was likely weaponized, I uploaded it to the Any.Run malware sandbox. Upon detonation, I observed a malicious macro quietly execute a hidden PowerShell command in the background, reaching out to an external server to download a secondary payload. 

3. **Connecting the Dots (Threat Intelligence):** 
   I ran the extracted IP addresses and file hashes through Open-Source Intelligence (OSINT) platforms like VirusTotal and AbuseIPDB. The global security community had already flagged this infrastructure for aggressive spam and malware distribution.

4. **Locking the Gates (Containment & Escalation):** 
   With the evidence gathered, I mapped the attack to the MITRE ATT&CK framework (**T1566.001 - Spearphishing Attachment**). I purged the email from the environment, recommended firewall blocks for the malicious IP, and wrote a comprehensive incident ticket to hand off to the Tier 2 team for a proactive threat hunt.

---

## 📁 Inside This Repository

I built this repository to mirror a real-world SOC environment. Here is what you will find inside:

* **`/Playbooks`:** The strict Standard Operating Procedures (SOPs) I follow to ensure every alert is investigated consistently and within strict SLAs.
* **`/Artifacts`:** The raw evidence I collected, including sanitized email headers, sandbox process trees, and VirusTotal API JSON data.
* **`/Incident_Tickets`:** My final escalation documentation (simulating a ServiceNow/Jira ticket), proving my ability to write clear, actionable intelligence reports for senior analysts.
* **`/Images`:** Visual proof of my hands-on work navigating industry-standard OSINT and threat intelligence platforms.

## 🛠️ My Tool Stack
* **Analysis & Sandboxing:** MXToolbox, Any.Run, manual header extraction
* **Threat Intelligence:** VirusTotal, AbuseIPDB, URLScan.io
* **Operations:** Splunk SIEM, Jira/ServiceNow ticketing, SANS Incident Response frameworks

---

## 📬 Let's Connect
I am actively seeking SOC Analyst roles where I can leverage my hands-on triage experience and passion for threat hunting. I am currently preparing for the **Microsoft SC-200 Security Operations Analyst** certification to further sharpen my SIEM engineering skills.

* **Email:** vishalsingh332001@gmail.com
* **LinkedIn:** [Insert your LinkedIn URL here]
