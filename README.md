# SOC Analyst L1 Portfolio

# Email Phishing Investigation - Fake IT Support Password Expiry

## 1. Objective
To analyze a suspicious email reporting a password expiry, determine if it is malicious, and extract indicators of compromise (IOCs) for blocking.

## 2. Email Details
- Subject: Action Required: Password Expires in 24 Hours
- Sender: it-support@helpdesk-update-portal.com
- Date Received: 12 Nov 2026
- Target: internal employee

## 3. Analysis Steps

### Header Analysis
Tool used: MXToolbox

<img width="821" height="364" alt="image" src="https://github.com/user-attachments/assets/d3a54be2-b3d2-463c-a5d8-215c7922066a" />

- SPF: Pass
- DKIM: Pass
- DMARC: None
Note: SPF and DKIM passed because the attacker registered and controls the sending domain (helpdesk-update-portal.com).


### Originating IP
- IP: 138.226.239.233
- Checked against VirusTotal and AbuseIPDB.

  <img width="800" height="378" alt="virustotal ip reputation check" src="https://github.com/user-attachments/assets/c98d6b71-02ef-4d78-9724-ffb19685f381" />
  
  <img width="1600" height="800" alt="abuseipdb reputation" src="https://github.com/user-attachments/assets/36936cd4-d484-46cf-bef8-cd9cfdb6f860" />


- Result: Flagged by 12 vendors for spam and phishing.

### URL Analysis
- Suspicious Link: https://secure-update-office365.com/login
- Tool used: URLScan.io
- <img width="904" height="413" alt="image" src="https://github.com/user-attachments/assets/ee2b59e3-f3a5-40bd-b563-09d3bb41cbff" />

- Findings: Domain was registered 2 days ago. The page hosts a fake Microsoft 365 login screen designed to steal credentials.

## 4. Conclusion
This is a true positive credential harvesting phishing attack. The attacker spoofed an IT alert to create urgency.

## 5. Actions Taken
- Blocked sender domain (helpdesk-update-portal.com) on email gateway.
- Blocked malicious URL (secure-update-office365.com) on web proxy.
- Blocked source IP on firewall.
- Escalated to L2 to verify if the receiving user clicked the link or submitted credentials.

- About Me-
Connect with me on LinkedIn:www.linkedin.com/in/vishal-singh-b6aa32218 Contact on: 6302334628
