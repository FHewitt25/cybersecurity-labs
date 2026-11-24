# Lab 3: AAA, Email & FTP Access Control

**Tool:** Cisco Packet Tracer · **Focus:** Identity and access management

## Scenario
Configure authentication (who you are) and authorization (what you can do) for wireless access, email and file transfer at a company HQ.

## What I did
**Authentication: AAA / RADIUS**
- Enabled the AAA service on a RADIUS server and created individual user accounts.
- Configured laptops for **WPA2-Enterprise**, where each user logs in with their own credentials instead of a shared Wi-Fi password. Verified DHCP addressing on 192.168.50.0/24.

**Email services**
- Enabled SMTP and POP3 on the mail server (`mail.cyberhq.com`), created mailbox accounts, configured four clients and sent/received test mail.

**Authorization: FTP least privilege**
- Enabled FTP and created three users. Two received full rights (read, write, delete, rename, list); one user (`malia`) was given **no delete permission**.
- Downloaded and uploaded files with `ftp`, `dir`, `get`, and `put`.
- **Verified the restriction:** logged in as `malia` and tried to delete a file. The server denied it, as configured.

## Security takeaways
- Individual credentials (WPA2-Enterprise/RADIUS) give accountability that a shared password can't.
- **Least privilege:** give users only the permissions their job needs, then test that the limits actually hold.
- Classic FTP and POP3 send credentials unencrypted; in production I would use SFTP/FTPS and secure mail protocols.
