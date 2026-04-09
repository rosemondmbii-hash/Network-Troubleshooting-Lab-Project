![Screenshot ipconfig](https://github.com/user-attachments/assets/3f3b2dcf-5e3f-443f-8026-285525da5d78)
# Network-Troubleshooting-Lab-Project
Troubleshooting 
🧾 1. Project Overview

This project demonstrates a structured approach to diagnosing network connectivity issues using core command-line tools. The goal was to identify and isolate network problems across different layers, including local connectivity, internet access, and DNS resolution.

🎯 2. Objective

To troubleshoot and analyze network connectivity by:

Verifying IP configuration
Testing local network communication
Validating internet connectivity
Identifying DNS resolution issues
🛠️ 3. Tools & Commands Used
Windows Command Prompt
ipconfig
ping
tracert
🔬 4. Methodology (Step-by-Step Process)
Step 1: Check IP Configuration

Command used:

ipconfig

Purpose:

Verify if the system has a valid IPv4 address
Confirm DHCP is assigning an IP

Expected Outcome:

A valid private IP (e.g., 192.168.x.x)
Presence of a Default Gateway !
[Screenshot ipconfig](https://github.com/user-attachments/assets/fcf7b32a-d520-4b4e-bfaf-f566dc645c17)



Step 2: Test Local Network Connectivity 

Command used:

ping <default_gateway>

Example:

ping 192.168.1.1

Purpose:

Confirm communication with the local router

Interpretation:

Successful reply → Local network is functioning
Failure → Local connectivity issue
![Failed local network issue, ping 192 168 1 1](https://github.com/user-attachments/assets/173d0307-efe4-49e0-845d-14ea976fb027)




Step 3: Test Internet Connectivity

Command used:

ping 8.8.8.8

Purpose:

Check if the device can reach the internet

Interpretation:

Successful reply → Internet connectivity is available
Failure → Issue beyond local network (ISP/router)
![pinging 172 20 1 1 ](https://github.com/user-attachments/assets/b0f1c043-8137-4f03-aaa7-0df411696e40)



Step 4: Test DNS Resolution

Command used:

ping google.com

Purpose:

Verify domain name resolution

Interpretation:

Successful reply → DNS is working
Failure (but 8.8.8.8 works) → DNS issue
![Screenshot ping 8 8 8 8](https://github.com/user-attachments/assets/4aa4f6a3-47ea-4e1d-a704-cb9b63c5087f)



Step 5: Trace Network Path

Command used:

tracert 8.8.8.8

Purpose:

Identify the path packets take to reach the destination
Detect where delays or failures occur

Interpretation:

Early failure → Local or gateway issue
Mid-path failure → ISP/network issue
Complete trace → Path is healthy
![Tracert google com](https://github.com/user-attachments/assets/2ac27338-fac5-4c34-aa88-1d87d95f0d0e)
![Screenshot tracert 8 8 8 8](https://github.com/user-attachments/assets/25bcfcaa-40ea-4780-9f4f-042ccd29c374)





📊 5. Results

Example:
ipconfig output showing valid IPv4 and gateway
Successful ping to gateway
Successful ping to 8.8.8.8
DNS resolution results
Tracert showing network hops
🧠 6. Analysis

The troubleshooting process followed a layered approach:

A valid IPv4 address confirmed DHCP functionality
Successful ping to the default gateway verified local network connectivity
Successful ping to a public IP confirmed internet access
DNS testing helped determine whether name resolution was functioning correctly
Tracert analysis provided visibility into the network path and potential latency points

This structured method allowed for efficient isolation of issues at different layers of the network.

✅ 7. Conclusion

This project demonstrates a systematic approach to diagnosing network issues using fundamental networking tools. By following a logical sequence—IP configuration, local connectivity, internet reachability, and DNS resolution—it is possible to quickly identify and isolate the root cause of most network problems.
