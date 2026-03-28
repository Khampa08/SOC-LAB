# Brute Force Detection

## Objective
To simulate a brute force login attempt and detect it using Splunk logs.

---

## Attack Simulation

From Kali Linux, I attempted multiple login attempts on the Windows machine.

Tool used:
- Hydra / manual login attempts

---

## Detection in Splunk

### Query:
EventCode=4625

### Explanation:
- EventCode 4625 → Failed login attempt
- Multiple failed attempts → Indicates brute force activity

---

## Observations

- Multiple failed login logs were generated
- Logs were successfully ingested into Splunk
- Detection was visible in Search & Reporting

---

## Conclusion
This experiment helped me understand how brute force attacks appear in logs and how SOC analysts detect them using SIEM tools.
---
