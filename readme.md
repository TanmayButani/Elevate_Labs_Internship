# Cyber Security Internship – Task 1

## Task Title: Network Reconnaissance Using Nmap & Wireshark

This task demonstrates how to identify open ports within a local network using a TCP SYN scan (`nmap -sS`) and validate that activity using Wireshark packet analysis. The goal is to understand basic reconnaissance techniques and evaluate network exposure from an attacker’s perspective.

## Tools Used

- Nmap – for port scanning
- Wireshark – for analyzing network traffic
- Local network IP range (e.g., 192.168.29.0/24)

## Process Overview

### 1. Identify Local IP Range

The local IP address was identified to determine the network range (e.g., 192.168.29.0/24). This range was used for scanning all devices connected within the same subnet.

### 2. Run Stealth Scan with Nmap

A TCP SYN scan was performed on the identified network range. The results displayed multiple hosts and their open ports. These open ports may indicate active services running on those hosts, which could be potential attack vectors if not secured.

Command used : 

```bash
nmap -sS 192.168.29.0/24
```

**Nmap Scan Result:**

![Nmap Scan](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%201/nmap_scan.png)

### 3. Analyze Traffic with Wireshark

During the scan, Wireshark captured packets to observe the behavior of the SYN scan. By applying appropriate filters, it was possible to see how Nmap sends SYN packets and identifies responsive hosts through SYN-ACK replies. The traffic shows incomplete TCP handshakes typical of stealth scans.

**Wireshark Filter Output:**

Filter used :

```bash
tcp.flags.syn == 1 && tcp.flags.ack == 0
```

![Wireshark Scan](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%201/wireshark_filter.png)

# 📧 Phishing Email Analysis – Internship Task 2

## 🎯 Objective:
Analyze a suspicious phishing email sample to identify potential threats, spoofing, and social engineering tactics.

---

## 🕵️‍♂️ Overview

As part of the Cyber Security Internship Task 2, I analyzed a phishing email sample pretending to be from **MetaMask**. The email subject was:

> **[IMPORTANT] Your wallet has been Blocked**

### 📝 Sample Screenshot

![Email Header](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%202/Phishing_1.png)

Spoofed MetaMask sender using suspicious domain kommunal.se

![Email Body](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%202/Phishing_2.PNG)

This email is a phishing attempt, using a sense of urgency and threats of losing funds to pressure users into clicking a suspicious "upgrade" link. Legitimate cryptocurrency wallet updates are performed directly within the application and never require you to follow a link from an email.


---

## 🔍 Key Findings

| Indicator | Observation |
|----------|-------------|
| **Sender Spoofing** | The email claimed to be from **MetaMask**, but the sender address was `info@kommunal.se` (a Swedish labor union domain, unrelated to MetaMask). |
| **Urgency Tactic** | The subject line used threatening language – *“Your wallet has been Blocked”* – to invoke fear. |
| **Suspicious Links** | Hyperlink in the email: `https://one-lnk.com/...` which does not belong to MetaMask. |
| **Design Mismatch** | Branding, formatting, and language do not match official MetaMask communication. |
| **Social Engineering** | Scares users with permanent crypto loss if no action is taken by a specific date. |

---

## 🔗 Tools Used

- **Email Client Viewer** (for header extraction)
- **Visual Inspection** of links and design
- **Browser inspection** of URLs

---

## 💡 Learning Outcome

This task helped me understand how phishing emails work, how to trace spoofed domains via headers, and how social engineering is used to trick users into clicking malicious links. It also taught me how to verify authenticity using tools like SPF/DKIM checks and header analyzers.


---

