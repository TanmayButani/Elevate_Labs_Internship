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
