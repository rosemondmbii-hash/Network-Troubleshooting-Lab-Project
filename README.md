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
![Screenshot IP Config](https://github.com/user-attachments/assets/87b2feb6-65f6-46ad-ae94-b1d922accadb)
My findings shows that IP address is present meaning DHCP is active and working.

Step 2: Test Local Network (Gateway)
Command:
ping <default gateway>

✅ Success → Local network OK
❌ Fail → Router / local network issue
![pinging 172 20 1 1 ](https://github.com/user-attachments/assets/4008f51f-89d5-4fee-ae10-58ee0ebf3647)
![IP Config all](https://github.com/user-attachments/assets/899a9ded-e81e-4e28-9df2-52c278ea4c97)
![Failed local network issue, ping 192 168 1 1](https://github.com/user-attachments/assets/3fe7fbb4-acad-4d0c-9404-e2d2b61adb04)
Based on the findings from the above image, connection to the local network with the gateway address of 192.168.1.1 reveals a failed router connection on the local network and the other image reveals a successful router connection to the local network.

Step 3: Test Internet Connectivity
Command:

ping 8.8.8.8

✅ Success → Internet is reachable
❌ Fail → ISP / external connectivity issue
![Screenshot ping 8 8 8 8](https://github.com/user-attachments/assets/942f7103-0744-4212-8667-ac2220af2ff5)
Findings reveals the internet is reachable to the ISP

Step 4: Test DNS Resolution
Command:

ping google.com

✅ Success → DNS working
❌ Fail (but 8.8.8.8 works) → DNS issue
![pinging google com](https://github.com/user-attachments/assets/7573e382-1bf1-488a-84ad-ecd39b243550)
Findings reveals a successful DNS working


