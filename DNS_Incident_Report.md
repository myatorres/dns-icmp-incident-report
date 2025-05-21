# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Summary of Problem in DNS and ICMP Logs

**The UDP protocol reveals that:**  
The system attempted to resolve a domain (`yummyrecipesforme.com`) by contacting a DNS server at `203.0.113.2` over UDP port 53.

**ICMP response indicates:**  
Each DNS query resulted in an ICMP error message: `"udp port 53 unreachable"`.

**Port 53 is used for:**  
Handling DNS queries over UDP.

**Most likely issue:**  
DNS server at `203.0.113.2` is either down, misconfigured, or UDP requests are blocked (e.g., firewall filtering).

---

## Part 2: Incident Analysis

**Time incident occurred:**  
- First attempt: `13:24:32`
- ICMP error received: `13:24:36`
- Repeated attempts every ~2 minutes

**How IT became aware:**  
Users reported an inability to access external websites using hostnames.

**Actions taken:**  
- Performed `tcpdump` network capture
- Identified multiple outbound DNS queries to `203.0.113.2`
- Observed no DNS responses, only ICMP error messages

**Key findings:**  
- DNS queries sent over UDP port 53
- No successful responses
- ICMP indicates the port is unreachable

**Likely cause of incident:**  
The DNS server may be offline, improperly configured, or filtering UDP traffic on port 53.

---

### Recommendations

- Check Firewall for UDP port 53 is open
- Check DNS service status on 203.0.113.2
