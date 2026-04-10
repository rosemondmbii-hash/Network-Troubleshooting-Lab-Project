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

Ping Gateway

➡️ Successful reply confirms local network connectivity

Ping Internet (8.8.8.8)

➡️ Confirms external internet access

Ping Domain (google.com)

➡️ Used to validate DNS resolution

Traceroute

➡️ Shows path packets take across network


