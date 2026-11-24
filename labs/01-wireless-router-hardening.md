# Lab 1: Wireless Router Hardening

**Tool:** Cisco Packet Tracer · **Focus:** Network hardening

## Scenario
A home/small-office wireless router was installed with insecure defaults. My job was to harden it and confirm only authorized devices could connect.

## What I did
1. **Changed the default admin password.** Default credentials are public; anyone who finds the router's IP can look them up.
2. **Disabled remote management.** An open management port invites password attacks. If remote access is truly needed, a VPN is the safer option.
3. **Broadcast a named SSID (HomeNet).** Hiding the SSID is not real security; sniffing tools still find "hidden" networks.
4. **Enabled WPA2-Personal with AES encryption** on every band so wireless traffic can't be read in transit.
5. **Created a separate GuestNet** (WPA2/AES) to keep visitor devices off the main network.
6. **Connected laptops and IoT devices** (webcam, siren, door sensor) with WPA2-PSK and verified DHCP addressing.
7. **Tested guest isolation.** A guest laptop could initially ping a home laptop. I disabled "allow guests to access the local network" and confirmed the pings then failed.

## Security takeaways
- Defaults (credentials, remote admin) are the first thing attackers check.
- Encryption (WPA2/AES) matters more than hiding the network name.
- **Network segmentation:** guest and IoT traffic should not reach internal hosts. I verified this with a test instead of assuming it worked.
