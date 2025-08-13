# 🛡 Task 3: Nessus Vulnerability Scan

## 🎯 Objective:
Perform a basic vulnerability scan on a personal computer using Nessus Essentials to identify potential security risks, document them, and propose possible mitigations.

---

## 🛠 Tools Used
- **Nessus Essentials** – Free vulnerability scanner by Tenable.
- **Target** – Localhost / internal network IP.
- **Operating System** – Microsoft Windows Server 2019.

---

## 📋 Process Overview

1. **Installation of Nessus Essentials**
   - Downloaded Nessus Essentials from [Tenable](https://www.tenable.com/products/nessus/nessus-essentials).
   - Installed and activated the free license key.

2. **Configuration of Scan**
   - Chose **Basic Network Scan** profile.
   - Set target IP to the local machine IP: `192.168.202.128`.
   - Selected full port scan with service detection enabled.

3. **Execution of Scan**
   - Launched scan and allowed it to run until completion (~9 minutes).
   - Scan detected 25 vulnerabilities (including Info level).

4. **Exporting and Analyzing Report**
   - Exported results in PDF format [Task-3 Nessus Scan PDF](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%203/Task-3.pdf)
   - Categorized vulnerabilities by severity:  
     - **Medium**: 2 findings  
     - **Low**: 1 finding  
     - **Informational**: 22 findings

---

## 📊 Key Findings

| Severity | Vulnerability | CVSS | Description |
|----------|--------------|------|-------------|
| **Medium** | SMB Signing not required | 5.3 | SMB protocol does not require signing, increasing risk of MITM attacks. |
| **Medium** | SSL Certificate Cannot Be Trusted | 6.5 | SSL certificate is self-signed or untrusted, which can be exploited in phishing/MITM scenarios. |
| **Low** | ICMP Timestamp Request Remote Date Disclosure | 2.1 | System reveals timestamp which could help in OS fingerprinting. |
| **Info** | Multiple service and OS detections | N/A | General system information disclosure such as OS version, open ports, supported protocols. |

---

## 🔧 Recommended Mitigations

- **SMB Signing not required** – Enable SMB signing via Group Policy to prevent tampering.
- **SSL Certificate Cannot Be Trusted** – Replace with a certificate from a trusted CA.
- **ICMP Timestamp Disclosure** – Disable ICMP timestamp responses via firewall rules.
- **Service Enumeration** – Restrict unnecessary services and use a firewall to limit external exposure.

---

## 📎 Screenshots
![Nessus Scan Screenshot](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%203/Nessus_Scan.png)

---

## 📄 Report
- [Task-3 Nessus Scan PDF](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%203/Task-3.pdf)

---

## 💡 Learning Outcome
This task provided hands-on experience in:
- Setting up and running a vulnerability scan.
- Understanding CVSS scoring and severity levels.
- Identifying common misconfigurations (SMB, SSL, ICMP).
- Mapping vulnerabilities to appropriate remediation steps.

---
