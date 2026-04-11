# Network Troubleshooting Lab Project

## 📌 Project Overview
This project demonstrates practical network troubleshooting using Windows command-line tools. The lab simulates a real-world scenario where a user experiences internet connectivity issues, and a structured troubleshooting approach is applied to identify the root cause.

---

## 🎯 Scenario

A user reports:
- Connected to Wi-Fi
- Unable to access websites

### Objective:
Identify whether the issue is caused by:
- DHCP failure
- Local network issue
- Internet connectivity problem
- DNS resolution failure

---

## 🛠️ Tools Used

- `ipconfig`
- `ping`
- `tracert`
- `ipconfig /all`
- `ipconfig /release`
- `ipconfig /renew`
- ```markdown
- `nslookup`

---

## 🔍 Troubleshooting Methodology

### Step 1: Check IP Configuration
Command:
```bash
ipconfig
✅ If IP address is present → DHCP is working
❌ If no IP → DHCP issue

Step 2: Test Local Network Gateway
Command:
ping default gateway
✅ Success → Local network OK
❌ Fail → Router / local network issue


Step 3: Test Internet Connectivity
Command:
ping 8.8.8.8
✅ Success → Internet is reachable
❌ Fail → ISP / external connectivity issue


Step 4: Test DNS Resolution
Command:
ping google.com
✅ Success → DNS working
❌ Fail (but 8.8.8.8 works) → DNS issue

Step 5: Trace Network Path
Command:
tracert google.com
Used to identify where packets drop along the path.

Step 6: DNS Lookup Test
Command:
```bash
nslookup google.com


🧠 Troubleshooting Decision Flow
No IP Address?
   → DHCP Issue

Can’t Ping Gateway?
   → Local Network Issue

Can’t Ping 8.8.8.8?
   → Internet Issue

Can Ping 8.8.8.8 but NOT google.com?
   → DNS Issue)


📄 Sample Ticket Documentation

Issue: User unable to access websites
Findings:

IP address assigned successfully

Gateway reachable

Internet reachable (8.8.8.8 successful)

Domain resolution failed

Root Cause: DNS resolution issue

Action Taken:

Verified DNS settings

Flushed DNS cache (if applicable)

Escalated if issue persists


💼 Real-World Application

This troubleshooting approach is used by:

Help Desk Technicians

Network Support Engineers

SOC Analysts (initial triage)

It helps:

Quickly isolate issues

Reduce resolution time

Improve customer experience

Provide accurate escalation details


🚀 Skills Demonstrated

Network troubleshooting

TCP/IP fundamentals

DNS analysis

Connectivity testing

Command-line diagnostics

Root cause analysis

Technical documentation



![Tracert google com](https://github.com/user-attachments/assets/75bbf54b-ddd0-4ce9-80f7-502f19da7c07)
![Screenshot tracert 8 8 8 8](https://github.com/user-attachments/assets/e9a89f57-a480-48a3-ac80-5376994d8d18)
![Screenshot ping 8 8 8 8](https://github.com/user-attachments/assets/be519a31-7aef-4af4-887f-aaed93c0d416)
![Screenshot of output](https://github.com/user-attachments/assets/3f0f0b31-efc1-4f9d-bce2-0e6b234c36e3)
![Screenshot ipconfig](https://github.com/user-attachments/assets/436554ea-bf74-4979-8b1f-d4f4dc1bd7ad)
![pinging google com](https://github.com/user-attachments/assets/569fab3e-3b5a-4d55-93ad-e422f456a86b)
![pinging 172 20 1 1 ](https://github.com/user-attachments/assets/ccf8e7bd-1237-445f-bf5a-ba53458e82d1)
![IP Config -renew](https://github.com/user-attachments/assets/1a12e92a-de3c-4adf-82bb-2113f8954600)
![IP Config -release](https://github.com/user-attachments/assets/2410185e-9c03-431e-8e11-630836ee9b64)
![IP Config all](https://github.com/user-attachments/assets/435cdc8b-ab59-481f-b125-f33bf6651b7e)
![IP Config all](https://github.com/user-attachments/assets/849df00d-1f1c-4a2a-82ac-feab1f5f34c8)
![Failed local network issue, ping 192 168 1 1](https://github.com/user-attachments/assets/117bcdc7-0fb7-4c1d-9a9e-e4d2ed95b792)
![Screenshot IP Config](https://github.com/user-attachments/assets/9a85e761-cbc2-4513-b2cc-2faa68501acd)
