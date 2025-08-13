# Task 4: Setup and Use a Firewall on Windows

## 🎯 Objective:
Configure and test basic firewall rules to allow or block traffic using Windows Firewall.

## 🛠 Tools Used:
- **Windows Defender Firewall with Advanced Security**
- **Telnet (for testing blocked port)**

## 📸 Deliverables:
Screenshots showing firewall rules created and applied.

---

## 📋 Steps Followed:

### 1. Viewed Current Outbound Firewall Rules
- Opened `Windows Defender Firewall with Advanced Security`.
- Navigated to **Outbound Rules** to view existing rules.

---

### 2. Created a New Outbound Rule to Block Telnet (Port 23)

#### a. **Rule Type**: Selected `Port`  
![Step1.png](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%204/Step1.png)

#### b. **Protocol and Port**: 
- Selected `TCP`
- Chose `Specific remote ports`: **23**
  
![Step2.png](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%204/Step2.png)

#### c. **Action**: Selected `Block the connection`  
![Step3.png](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%204/Step3.png)

#### d. **Profile**: Applied rule to all profiles (`Domain`, `Private`, `Public`)  
![Step4.png](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%204/Step4.png)

#### e. **Name**: Named the rule as `TelnetBlockTest`  
![Step5.png](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%204/Step5.png)

---

### 3. Tested the Rule:
- Tried connecting using Telnet to verify the port was blocked.
- Confirmed connection was blocked successfully.

---

### 4. (Optional but recommended): Removed the Rule after Testing
- Disabled or deleted the `TelnetBlockTest` rule to restore original firewall settings.

---

### 🧪 How Firewall Filters Traffic:

- **Inbound Rules**: Control traffic *coming into* the system.
- **Outbound Rules**: Control traffic *going out* of the system.
- You can filter based on:
  - Application/program
  - Specific port (TCP/UDP)
  - IP addresses (local/remote)
  - Network profile (Domain, Private, Public)

---

## ✅ Outcome:
- Learned how to configure and apply basic firewall rules.
- Successfully tested port blocking and understood how Windows Firewall filters traffic.

---

## 📁 Files and Screenshots:
- `Step1.png` to `Step5.png` – Step-by-step GUI configuration

---
