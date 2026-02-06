## Scenario
You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a denial of service (DoS) attack. 

To address this security event, the network security team implemented: 

A new firewall rule to limit the rate of incoming ICMP packets

Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets

Network monitoring software to detect abnormal traffic patterns

An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security, following the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). You will use the CSF to help you navigate through the different steps of analyzing this cybersecurity event and integrate your analysis into a general security strategy. 

## Response:
### Summary
The organization experienced a DoS attack using ICMP requests that disabled the internal network for 2 hours. This was possible because of an unconfigured firewall.

### Identify
The attack affected the internal network and blocked employees' access to work tools. The team found that the main vulnerability was the unconfigured firewall.

### Protect
The team implemented a new firewall rule for ICMP packet rate limiting and source IP verification to prevent IP spoofing. We also installed an IPS as a protective technology to automatically filter suspicious traffic. The company will update maintenance procedures for hardware and software and provide awareness training for all employees.

### Detect
In the future, the team will use new monitoring software and an IDS (Intrusion Detection System) to scan for abnormal traffic patterns and detect security events. We can also use a SIEM tool to send alerts to the security team when an anomaly is found.

### Respond
The team will isolate affected systems to prevent further disruption. We will attempt to restore critical systems first. Then, the team will analyze network logs to check for suspicious activity and report incidents to management.

### Recover
To recover from a future ICMP flood attack, we need to restore network services to a normal state. First, the attack should be blocked at the firewall. Then, we should stop all non-critical services to reduce traffic. Critical services must be restored first. Finally, when the traffic is normal, we can bring back non-critical systems.
