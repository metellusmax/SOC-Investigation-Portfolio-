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
The attachment name looks like a MD5 hash. I search the name of the name of the file in Virus Total and Hybrid Analysis and gotten no hits. 
<img width="1886" height="672" alt="image" src="https://github.com/user-attachments/assets/3113d0eb-f28b-45bf-a8a1-e136cbcbc832" />

Next I went ahead and downloaded the file from the email and it was a double zip file. Unzip the file and noticed there were 3 files. 2 DLL files and an XLS file. 

<img width="622" height="280" alt="image" src="https://github.com/user-attachments/assets/159c2db9-2268-4c66-abdf-822bf4177065" />

Then I took the hash of the XLS file and check to see if virus total or Hybrid analysis have any hits.  
<img width="1885" height="917" alt="image" src="https://github.com/user-attachments/assets/e63d6faf-f7d2-4b73-a831-132bfb3cb589" />
<img width="1577" height="927" alt="image" src="https://github.com/user-attachments/assets/4b28455b-7ee4-449a-8856-a16c7a267eea" />
After referencing both sites it looks like this file was malicious. Next we need to find out if the recipient opened the email and were there any malicious activities. When checking the log files in Log Management I searched Lars system IP and notices 2 suspicious connections to 2 external IP addresses.   
<img width="1447" height="210" alt="image" src="https://github.com/user-attachments/assets/1b4cf6aa-cefd-4197-bcdd-ae0b7300e08d" />
Both of the sites is linked to the malicious XLS file that was found in the email and we also see in Endpoint security we noticed the DLL files were ran per the system Terminal history. 

<img width="1890" height="772" alt="image" src="https://github.com/user-attachments/assets/58566e39-bf8e-4d07-b35a-3594c19e839c" />
<img width="612" height="332" alt="image" src="https://github.com/user-attachments/assets/f6797b94-dd38-48b5-aedf-d3a53fe87417" />
<img width="625" height="325" alt="image" src="https://github.com/user-attachments/assets/ca44e166-9188-4a85-9b35-7c4f1f98ee88" />

<img width="920" height="462" alt="image" src="https://github.com/user-attachments/assets/ab57c8fc-5be0-49ae-bd6e-889f92961989" />

With these finding we were able to see Lars system was infected and we needed to get it isolated before it can infect other system or continue to do damage.

<img width="1212" height="417" alt="image" src="https://github.com/user-attachments/assets/35d8d92a-4b62-4e9e-af52-5d52d16cc4ee" />










### Artifacts

<img width="1086" height="575" alt="image" src="https://github.com/user-attachments/assets/38ff5e09-a1ed-44ff-a536-6cab268b99f0" />


### PlayBook




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

