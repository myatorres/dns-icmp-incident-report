# DNS Incident Report - Google Cybersecurity Certificate

This project is part of the Google Cybersecurity Professional Certificate course. It documents the analysis and reporting process for a simulated DNS failure scenario.

## Scenario Summary

Several users were unable to access the website `yummyrecipesforme.com`. The error message “destination port unreachable” indicated a DNS resolution issue. As a cybersecurity analyst, I used `tcpdump` to capture network traffic and analyze the DNS and ICMP logs.

## Report Summary

- The client attempted to resolve `yummyrecipesforme.com` via DNS server `203.0.113.2`.
- Repeated DNS queries were sent using UDP on port 53.
- Each query failed, and an ICMP error message (`udp port 53 unreachable`) was returned.
- Indicates DNS server is down, misconfigured, or firewall-blocked.

## Tools Used

- `tcpdump`
- DNS protocol
- ICMP traffic analysis
- Markdown for reporting

##  Files

- **`DNS_incident_report.md`**: Typed version of the final report using the provided template.
- **`/screenshots/`**: Contains original screenshots from the scenario and my completed report.

## Screenshots

The `/screenshots` folder includes:
- **`tcpdump_logs.png`**: Tcpdump logs showing DNS queries and ICMP responses
- **`exmaple_scenario.png`**: Screenshot of exmaple scenario from the course activity
- **`exmaple_incident_report.png`**: Example template of final report sctructure given from the activity
- **`cybersecurity_incident_report_final.png`**: Screenshot of my own completed report using the template provided

## What I Learned & Skills Applied

- How to analyze DNS failure using `tcpdump`
- Network traffic analysis
- DNS & ICMP interpretation
- Creating structured incident reports

---

*This project is for educational purposes only as part of a course lab activity.*
