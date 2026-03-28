# SOC-LAB Project

## Overview
This project is a hands-on Security Operations Center (SOC) lab built using Kali Linux, Windows 10, and Splunk. The goal of this lab is to understand how attackers operate and how defenders detect and analyze those activities using a SIEM tool.
Instead of only learning theory, this lab focuses on practical experience like network setup, log monitoring, and basic threat detection.

## Lab Setup
I created this lab using Oracle VirtualBox with two virtual machines:
- Kali Linux → Used as the attacker machine  
- Windows 10 → Used as the target machine  
- Splunk Enterprise → Installed on Windows for log monitoring  

### Network Configuration
- NAT adapter → For internet access  
- Internal Network → For communication between Kali and Windows  
- Manual IP configuration used  

Example:
- Windows: 192.168.1.10 
- Kali: 192.168.1.20 
This setup ensures both machines can communicate securely inside the lab.

## What I Did in This Lab
### 1. Network Connectivity
First, I verified that both machines can communicate using ping.

### 2. Port Scanning
I used Nmap from Kali Linux to scan the Windows machine and identify open ports.
This helped me understand:
- Running services
- Open attack surface

### 3. Log Collection (SIEM Setup)
Installed Splunk on Windows and enabled:
- Windows Event Logs
- Security logs
These logs are used to monitor system activity.

### 4. Log Analysis
Used Splunk Search & Reporting to explore logs and understand system behavior.

## Detection Use Case — Failed Login Attempts
One simple detection I implemented is identifying failed login attempts.

### Splunk Query:EventCode=4625
### What it means:
- EventCode 4625 → Failed login attempt
- Multiple failed attempts → Possible brute force attack

This is a basic but important SOC detection scenario.

## Screenshots
### Network Connectivity
- Ping from Kali to Windows

### Port Scanning
- Nmap scan results showing open ports

### Splunk Logs
- Windows event logs inside Splunk
- Detection of failed login attempts

(All screenshots are available in the screenshots folder)

## Skills Learned

Through this project, I gained practical experience in:
- Virtual lab setup (VirtualBox)
- Network configuration (NAT & Internal Network)
- Basic penetration testing (Nmap)
- SIEM usage (Splunk)
- Log analysis and detection

## Challenges Faced
- Configuring internal network correctly  
- Understanding Splunk data ingestion  
- Learning how Windows logs work  

Solving these helped me understand real-world SOC environments better.

## Future Improvements
- Create custom alerts in Splunk  
- Build dashboards  
- Simulate brute force attacks  
- Integrate tools like Wazuh  

---

## Conclusion
This project helped me move from theory to practical cybersecurity skills. It gave me a clear understanding of how attackers generate activity and how defenders monitor and detect it using logs.

This is just the beginning, and I plan to expand this lab with more advanced detection scenarios.
---
