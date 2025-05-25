# Cybersecurity Incident Report

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log

The network protocol analyzer logs show multiple attempts to resolve the domain `www.yummyrecipesforme.com` using DNS over UDP port 53. Each attempt received an ICMP response indicating that port 53 was unreachable. Port 53 is standard for handling DNS queries, and an “unreachable” response typically points to issues such as a service outage, firewall restrictions, or a misconfiguration. This behavior suggests that the DNS requests could not be delivered, preventing the website from loading for users.

## Part 2: Explain your analysis of the data and provide at least one cause of the incident

The issue was initially reported around 1:24 PM when multiple clients indicated that they were unable to access the website `www.yummyrecipesforme.com`, receiving a “destination port unreachable” error. Follow-up attempts at 1:26 PM and 1:28 PM resulted in the same error. 

The network security team responded by capturing traffic using `tcpdump` while trying to access the site. The analysis of the captured logs confirmed that DNS queries sent over UDP port 53 did not reach the DNS server. Instead, ICMP error messages were returned, indicating that port 53 was unreachable. 

One possible explanation is that a firewall is blocking outbound DNS requests or that there is a misconfiguration on the DNS server or intermediary network devices. Next steps include checking the firewall settings, verifying the DNS server’s availability, and collaborating with system administrators to rule out service outages or unauthorized configuration changes.
