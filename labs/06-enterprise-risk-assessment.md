# Lab 6: Enterprise Cybersecurity Risk Assessment

**Focus:** Risk assessment and governance

## Scenario
Athena Learning, a fictional e-learning company with about 110 staff across three offices. It stores student PII and payment data, runs its own SQL databases, web portals, DNS and email, allows BYOD, and supports remote employees.

## What I did
Built an asset → threat → mitigation register across information, software and physical assets. Highlights:

| Asset | Threats | Mitigations |
|---|---|---|
| Student PII on servers | Data theft, identity theft | Encrypt stored data, access controls |
| Student payment data | Credit card theft, identity theft | Encryption at rest |
| Course content and website | Unauthorized access, data theft, content tampering | Strong authentication, web app hardening |
| Partner uploads | Tampering, theft in transit | VPN, hashing to verify integrity |
| Remote-worker access | Data theft, tampering | VPN |
| Host operating systems | Malware, phishing, malicious sites, unpatched vulnerabilities | Antivirus, web filtering, user training, patching |
| SQL databases | SQL/XML injection, data-entry errors | Input validation |
| Web server software | Unpatched vulnerabilities, cross-site scripting | Patching |
| In-house applications | Application exploits | Secure development, strong input validation |
| Laptops | Loss, theft, drive failure | Drive encryption, host firewall, backups |
| Desktops and servers | Power loss, hardware failure, physical access | Power protection, backups, badge/biometric access |

## Security takeaways
- You can't protect what you haven't inventoried, so the asset list comes first.
- Most threats map to a small set of controls: **encryption, patching, input validation, backups, access control and training**.
- BYOD and remote work widen the attack surface; VPNs and endpoint controls help close it.
