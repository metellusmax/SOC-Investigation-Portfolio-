# LD-001: Phishing Email with Malicious Excel 4.0 Macro Attachment

## Alert Details

<img width="1493" height="350" alt="image" src="https://github.com/user-attachments/assets/d7de55ab-d61e-4813-8f72-c2790c5d0f79" />


# Executive Summary

A high-severity phishing alert was generated after user Lars received a suspicious email from trenton@tritowncomputers.com with the subject "RE: Meeting Notes." The email contained a ZIP archive
attachment that included an Excel 4.0 macro-enabled spreadsheet and two DLL files. Analysis of the attachment identified that the attachment includes an Excel 4.0 macro-enabled spreadsheet and two DLL files.
Investigation revealed that the user opened the attachment, subsequently accessed suspicious external URLs and the suspicious DLL were ran. Due to the risk of system compromise, Lars' workstation
was quarantined to prevent further malicious activity while the investigation was conducted. Based on the collected evidence, the alert was classified as a true positive phishing incident.
Would recommend Security awareness training to reduce the risk of future phishing-related incidents.



---

# Alert Details

<img width="1493" height="350" alt="image" src="https://github.com/user-attachments/assets/d7de55ab-d61e-4813-8f72-c2790c5d0f79" />


---

# Initial Triage

After claiming the ticket 1st step I looked to find the email in question in LetsDefend Email Security, I found a suspicious attachment. 
<img width="1575" height="555" alt="image" src="https://github.com/user-attachments/assets/73e1520d-1c56-436d-8778-072db4185b74" />
The attachment name looks like a MD5 hash. I confirm my suspicion by downloading the file from the email and it was a double zip file. 


## Observations

Document the indicators that initially made the alert suspicious.

- Suspicious sender
- Unexpected attachment
- External URL present
- Known malicious hash
- Failed SPF/DKIM
- User reported suspicious email

---

# Email Analysis

## Sender Analysis

| Item | Result |
|---------|---------|
| Sender Address | |
| Domain | |
| Reputation | |
| SPF Result | |
| DKIM Result | |

### Findings

Document any suspicious sender characteristics.

---

## Subject Analysis

**Subject:**

```
Insert email subject
```

### Findings

Document whether the subject appears suspicious or attempts to create urgency.

---

# Attachment Analysis

## Attachment Details

| File Name | File Type | SHA256 |
|------------|------------|------------|
| | | |

### Findings

Document:

- File type
- Hash reputation results
- Suspicious behavior
- Presence of macros
- Malware indicators

---

# URL Analysis

## URLs Identified

| URL | Reputation | Notes |
|------|------|------|
| | | |

### Findings

Document:

- Redirect behavior
- Domain reputation
- Phishing indicators
- Credential harvesting attempts

---

# Threat Intelligence

## VirusTotal

### Result

- Detection Ratio:
- Community Score:
- First Seen:

### Findings

Document VirusTotal findings.

---

## Additional Sources

### URLScan

### AbuseIPDB

### Hybrid Analysis

### Any.Run

Document any intelligence gathered from external sources.

---

# Indicators of Compromise (IOCs)

## IP Addresses

| IOC | Type |
|------|------|
| | |

## Domains

| IOC |
|------|
| |

## URLs

| IOC |
|------|
| |

## File Hashes

| File | Hash |
|------|------|
| | |

---

# Investigation Process

## Step 1: Alert Review

Describe actions performed.

### Findings

---

## Step 2: Email Analysis

Describe actions performed.

### Findings

---

## Step 3: Attachment Analysis

Describe actions performed.

### Findings

---

## Step 4: Threat Intelligence Research

Describe actions performed.

### Findings

---

## Step 5: Final Assessment

Describe actions performed.

### Findings

---

# MITRE ATT&CK Mapping

| Technique | Description |
|------------|-------------|
| T1566 | Phishing |
| T1566.001 | Spearphishing Attachment |
| T1566.002 | Spearphishing Link |
| T1204 | User Execution |

> Include only the techniques applicable to the investigation.

---

# Risk Assessment

| Category | Assessment |
|-----------|-----------|
| Likelihood | Low / Medium / High |
| Impact | Low / Medium / High |
| Risk Level | Low / Medium / High |

---

# Remediation Recommendations

- Quarantine the email
- Block sender address
- Block malicious domains
- Block malicious URLs
- Block file hashes
- Conduct endpoint review
- Notify affected users

---

# Conclusion

Summarize:

- What happened
- What was discovered
- Whether the alert was malicious
- Recommended actions

---

# Lessons Learned

Document key takeaways from the investigation.

### Example

- Excel 4.0 macros remain a common malware delivery technique.
- Hash reputation checks should be combined with behavioral analysis.
- Multiple threat-intelligence sources improve confidence in findings.

---

# Screenshots

## Alert Overview

![Alert Overview](screenshots/alert-overview.png)

## VirusTotal Results

![VirusTotal](screenshots/virustotal-results.png)

## Email Details

![Email Details](screenshots/email-details.png)

---

# Analyst

**Max Metellus**

