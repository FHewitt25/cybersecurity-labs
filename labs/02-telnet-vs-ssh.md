# Lab 2: Telnet vs. SSH Remote Access

**Tool:** Cisco Packet Tracer · **Focus:** Secure protocols

## What I did
1. Verified the PC received an IP address from DHCP (`ipconfig`) and could ping the router (64.100.1.1).
2. Attempted **Telnet**: `telnet 64.100.1.1` → the connection was closed by the router. Telnet had been disabled on purpose.
3. Connected with **SSH**: `ssh -l admin 64.100.1.1` and authenticated successfully.

## Security takeaways
- Telnet sends usernames, passwords and commands in **plain text**, so anyone capturing traffic can read them.
- SSH encrypts the whole session and should be the only remote-admin protocol allowed.
- In a SOC, Telnet (TCP 23) traffic to network devices is worth flagging.
