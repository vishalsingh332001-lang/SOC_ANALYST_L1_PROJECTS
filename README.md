
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
- SPF: Pass
- DKIM: Pass
- DMARC: None
Note: SPF and DKIM passed because the attacker registered and controls the sending domain (helpdesk-update-portal.com).

### Originating IP
- IP: 138.226.239.233
- Checked against VirusTotal and AbuseIPDB.
- Result: Flagged by 14 vendors for spam and phishing.

### URL Analysis
- Suspicious Link: https://secure-update-office365.com/login
- Tool used: URLScan.io
- Findings: Domain was registered 2 days ago. The page hosts a fake Microsoft 365 login screen designed to steal credentials.

## 4. Conclusion
This is a true positive credential harvesting phishing attack. The attacker spoofed an IT alert to create urgency.

## 5. Actions Taken
- Blocked sender domain (helpdesk-update-portal.com) on email gateway.
- Blocked malicious URL (secure-update-office365.com) on web proxy.
- Blocked source IP on firewall.
- Escalated to L2 to verify if the receiving user clicked the link or submitted credentials.
