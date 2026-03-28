# Windows Logs Analysis

## Overview
In this lab, I collected Windows Event Logs and analyzed them using Splunk.

---

## Log Source

- Windows Event Viewer
- Log Type: Security & Application logs
- Forwarded to Splunk

---

## Important Event Codes

### 4625 – Failed Login
- Indicates failed login attempt
- Used to detect brute force attacks

### 4624 – Successful Login
- Indicates successful login
- Helps track user activity

---

## Example Splunk Queries

### Failed Login Attempts
EventCode=4625

### Successful Logins
EventCode=4624

---

## Observations

- Logs were successfully ingested into Splunk
- Failed login attempts were visible
- Multiple failed attempts indicate suspicious activity

---

## Conclusion

Windows logs are very useful for detecting attacks and monitoring system activity in a SOC environment.
