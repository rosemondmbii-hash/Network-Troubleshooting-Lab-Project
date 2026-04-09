
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
![pinging 172 20 1 1 ](https://github.com/user-attachments/assets/ca046a2d-e801-4be8-be11-69821186bf5c)



Step 3: Test Internet Connectivity

Command used:

ping 8.8.8.8

Purpose:

Check if the device can reach the internet

Interpretation:

Successful reply → Internet connectivity is available
Failure → Issue beyond local network (ISP/router)
![Screenshot ping 8 8 8 8](https://github.com/user-attachments/assets/1c1c6b0d-2a79-4b34-8b01-5569fe424a4e)



Step 4: Test DNS Resolution

Command used:

ping google.com

Purpose:

Verify domain name resolution

Interpretation:

Successful reply → DNS is working
Failure (but 8.8.8.8 works) → DNS issue
![pinging google com](https://github.com/user-attachments/assets/d98e1a3a-eccf-490e-9956-966988fd17a6)



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

other command lines learned

IP Config all 
shows more details of the network ( MAC Address, the different ethernet adapters, DHCP)
![IP Config all](https://github.com/user-attachments/assets/6b460ebb-f258-4541-b547-dd1101f15cf3)
![IP Config all](https://github.com/user-attachments/assets/8c9b82c4-fb70-4913-8ce3-19c332fa3cfa)

IP Config /renew
![IP Config -renew](https://github.com/user-attachments/assets/6a482d45-dac0-4bd6-b1a6-3021b3e1e8c5)

IP Config /release
![IP Config -release](https://github.com/user-attachments/assets/c5c30fee-057f-4ce9-a565-1ad08ede3f95)


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
