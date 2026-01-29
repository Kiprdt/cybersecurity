## Scenario
You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 

One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.

You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. 

You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.

## Incident Report
The website is unreachable because of a DoS attack. From the logs, we can see many half-opened TCP connections where the threat actor (203.0.113.0) sends only SYN flags and doesn't respond to the SYN-ACK. This is likely a SYN-flood attack and a DoS (not a DDoS) because the malicious requests are sent by only one IP.

### How the TCP handshake mechanism works:

- A visitor (198.51.100.23) sends a SYN packet to request a connection.

- The server (192.0.2.1) responds with a SYN-ACK packet.

- The visitor sends an ACK packet to establish the connection.

But if there is a large number of SYN packets overflowing the queue of half-opened connections, legitimate requests to connect will be impossible. Moreover, the logs indicate that visitors can't get responses because the server is exhausted by unfinished TCP requests, or they get error messages about connection timeouts because the server takes too long to respond.

## Recomendation
To prevent this problem from happening again, we will block the malicious IP address on the firewall. Also, we can implement an NGFW and use a cloud Anti-DDoS solution to filter malicious traffic and exclude the possibility of DoS attacks. Moreover, we can enable SYN cookies as an emergency measure to prevent an attack if other methods do not work.
