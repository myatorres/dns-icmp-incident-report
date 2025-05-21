# DNS & ICMP Network Traffic Incident Report

This project analyzes a DNS failure captured via `tcpdump` and documents the cause, timestamps, and ICMP responses indicating unreachable ports.

## Summary

- The client attempted to resolve `yummyrecipesforme.com` via DNS server `203.0.113.2`.
- Repeated DNS queries were sent using UDP on port 53.
- Each query failed, and an ICMP error message (`udp port 53 unreachable`) was returned.
- Indicates DNS server is down, misconfigured, or firewall-blocked.

## Project Structure

- `DNS_Incident_Report.md`: Full write-up of the investigation.
- `logs/`: Screenshots or pcap evidence.
- `analysis/`: Parsed notes and summary logs.

## Skills Applied

- Network traffic analysis
- DNS & ICMP interpretation
- Cyber incident reporting
