# 📧 Task 2: Phishing Email Analysis

## 🎯 Objective:
Analyze a suspicious phishing email sample to identify potential threats, spoofing, and social engineering tactics.

---

## 🕵️‍♂️ Overview

As part of the Cyber Security Internship Task 2, I analyzed a phishing email sample pretending to be from **MetaMask**. The email subject was:

> **[IMPORTANT] Your wallet has been Blocked**

### 📝 Screenshot
![Email Header](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%202/Phishing_1.png)

Spoofed MetaMask sender using suspicious domain kommunal.se

![Email Body](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Task%202/Phishing_2.png)

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

## 📎 Screenshots

- `screenshot-email-view.png` – User view of phishing email
- `screenshot-email-header.png` – Header showing spoofed sender

---

## 💡 Learning Outcome

This task helped me understand how phishing emails work, how to trace spoofed domains via headers, and how social engineering is used to trick users into clicking malicious links. It also taught me how to verify authenticity using tools like SPF/DKIM checks and header analyzers.
