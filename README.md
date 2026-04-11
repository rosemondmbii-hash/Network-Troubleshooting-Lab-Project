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
My findings shows that IP address is present meaning DHCP is active and working.

Step 2: Test Local Network (Gateway)
Command:
ping <default gateway>
✅ Success → Local network OK
❌ Fail → Router / local network issue
Based on the findings from the above image, connection to the local network with the gateway address of 192.168.1.1 reveals a failed router connection on the local network and the other image reveals a successful router connection to the local network.

Step 3: Test Internet Connectivity
Command:

ping 8.8.8.8

✅ Success → Internet is reachable
❌ Fail → ISP / external connectivity issue
Findings reveals the internet is reachable to the ISP

Step 4: Test DNS Resolution
Command:

ping google.com

✅ Success → DNS working
❌ Fail (but 8.8.8.8 works) → DNS issue
Findings reveals a successful DNS working

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
   → DNS Issue

📸 Evidence (Screenshots)
IP Configuration

➡️ Confirms valid IPv4 address assigned
![Screenshot IP Config](https://github.com/user-attachments/assets/40e4a55d-e732-49a5-9764-536bcfc85d76)

Ping Gateway
![pinging 172 20 1 1 ](https://github.com/user-attachments/assets/196d3374-fb33-48a2-af78-57f239e5c938)


➡️ Successful reply confirms local network connectivity

Ping Internet (8.8.8.8)
![Screenshot ping 8 8 8 8](https://github.com/user-attachments/assets/382fde51-fdcb-4e56-9483-4f124dd5d639)


➡️ Confirms external internet access

Ping Domain (google.com)
![pinging google com](https://github.com/user-attachments/assets/d2f68eb3-b3e4-4833-b43e-3c30625b0dbe)

➡️ Used to validate DNS resolution

Traceroute

➡️ Shows path packets take across network
![Tracert google com](https://github.com/user-attachments/assets/451de021-15c9-4744-bbcc-a52c86b820f6)
![Screenshot tracert 8 8 8 8](https://github.com/user-attachments/assets/ae55bb99-4667-4a12-abbd-c2a68fe4d308)



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

![pinging google com](https://github.com/user-attachments/assets/eb9cdde7-3b9a-484d-9eaa-768b32960a57)
