# Lab 8: Networking Fundamentals for Security Analysts

**Tool:** Cisco Packet Tracer · **Focus:** How traffic really moves, which is the foundation for reading logs and packet captures

| Lab | What I did | Why it matters in security |
|---|---|---|
| Create a LAN | Cabled devices, set IPv4 addresses, verified with `ipconfig` and `ping` | Baseline of how hosts are addressed |
| Configure DHCP on a wireless router | Set a custom DHCP range and moved clients to DHCP | DHCP logs map an IP to a device at a point in time, which is key in investigations |
| Examine NAT | Connected 4 PCs and traced traffic as private IPs were translated to the router's public IP | Many internal hosts share one public IP, so logs need NAT context to find the real source |
| Identify MAC and IP addresses | Followed PDUs locally and across routers | MAC addresses change at each hop; IP addresses stay end to end |
| Observe traffic in a routed network | Compared an unrouted LAN with one routed between segments | Routers split broadcast domains, which is the basis of segmentation |
| Connect to a web server | Followed packets across the internet by IP | End-to-end path of a web request |
| Use the ping command | Used `ping` to find a misconfigured PC | First step of any connectivity troubleshooting |

## Security takeaways
- To investigate an alert you have to know where traffic came from, and NAT, DHCP and MAC/IP behavior all shape what the logs show.
- Segmentation (routing and VLANs) limits how far an attacker can move, the same principle as in my [Splunk lab](https://github.com/FHewitt25/splunk-bruteforce-detection-lab).
