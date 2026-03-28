
# SOC Lab Architecture

## Overview
This lab consists of two virtual machines connected through an internal network and monitored using Splunk.

---

## Components

- Kali Linux (Attacker)
- Windows 10 (Target)
- Splunk Enterprise (SIEM)
- VirtualBox (Virtualization)

---

## Network Setup

- NAT Adapter → Internet access
- Internal Network → Communication between VMs

Example IPs:
- Kali Linux: 192.168.x.x
- Windows: 192.168.x.x

---

## Data Flow

1. Attacker (Kali) sends traffic → Windows
2. Windows generates logs
3. Splunk collects logs
4. Analyst searches & detects activity

---

## Diagram (Simple)

Kali Linux  --->  Windows  --->  Splunk
   (Attack)        (Logs)        (Detection)

---

## Conclusion

This architecture simulates a basic SOC environment where attack, logging, and detection happen in a controlled lab.
