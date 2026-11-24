# Cybersecurity Labs: Network Security, Access Control & Risk

Hands-on labs I completed during the **Per Scholas Cybersecurity program (Atlanta, 2026)**, written up in my own words: what I configured, the commands I used, and the security lesson from each one.

> Built in Cisco Packet Tracer and a Linux Security Workstation VM. Lab scenarios are from the Cisco Networking Academy curriculum; the write-ups and findings are mine.

## Lab index

| # | Lab | Focus | Key skills |
|---|---|---|---|
| 1 | [Wireless router hardening](labs/01-wireless-router-hardening.md) | Network hardening | Default credentials, remote mgmt, WPA2/AES, guest isolation |
| 2 | [Telnet vs. SSH remote access](labs/02-telnet-vs-ssh.md) | Secure protocols | SSH, insecure protocol identification |
| 3 | [AAA, email & FTP access control](labs/03-aaa-access-control.md) | Identity & access | RADIUS/AAA, WPA2-Enterprise, least privilege |
| 4 | [IoT physical security](labs/04-iot-physical-security.md) | IoT / physical security | Device registration, sensors, alarms |
| 5 | [Password cracking with fcrackzip](labs/05-password-cracking-fcrackzip.md) | Cryptography | Brute force, password length vs. time |
| 6 | [Enterprise risk assessment](labs/06-enterprise-risk-assessment.md) | Risk & governance | Asset inventory, threats, mitigations |
| 7 | [OWASP Top 10 investigation](labs/07-owasp-top-10.md) | Application security | Broken access control, injection, misconfiguration |
| 8 | [Networking fundamentals for analysts](labs/08-networking-fundamentals.md) | Networking | NAT, DHCP, MAC vs. IP, routing, ping |

## Why these matter for a SOC role
- **Hardening and access control** are what analysts check first when an alert fires: was the default password changed, was Telnet open, did the user have more rights than they needed?
- **Networking fundamentals** (NAT, DHCP, MAC/IP, routing) are how you read logs and packet captures and trace where traffic really came from.
- **Risk assessment and OWASP** connect technical findings to business impact, which is how incidents get prioritized.

## Related project
[Splunk Brute-Force Detection Lab](https://github.com/FHewitt25/splunk-bruteforce-detection-lab): detecting credential attacks in a segmented home SOC lab.

---
**Fabian Hewitt** · CompTIA Security+ · Splunk Core Certified Power User · [LinkedIn](https://www.linkedin.com/in/fabian-hewitt-792712250)
