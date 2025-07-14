# DDoS Attacks

**Last Updated:** 2025-07-15

A Distributed Denial of Service (DDoS) attack is a malicious attempt to disrupt the normal traffic of a targeted server, service, or network by overwhelming the target or its surrounding infrastructure with a flood of Internet traffic.

## Types of DDoS Attacks

DDoS attacks can be broadly categorized into three types:

### 1. Volume-Based Attacks

Volume-based attacks aim to saturate the bandwidth of the targeted site. The magnitude of the attack is measured in bits per second (bps).

*   **UDP Flood:** A UDP flood is a type of DDoS attack in which the attacker overwhelms the target with User Datagram Protocol (UDP) packets.
*   **ICMP Flood:** An ICMP flood, also known as a Ping flood, is a DDoS attack that overwhelms the target with ICMP Echo Request (ping) packets.
*   **DNS Amplification:** A DNS amplification attack is a DDoS attack in which the attacker uses open DNS resolvers to flood the target with DNS response traffic.

### 2. Protocol Attacks

Protocol attacks, also known as state-exhaustion attacks, cause a service disruption by consuming all the available state table capacity of web application servers or intermediate resources like firewalls and load balancers. The magnitude of the attack is measured in packets per second (pps).

*   **SYN Flood:** A SYN flood is a DDoS attack that exploits the TCP handshake process. The attacker sends a succession of SYN requests to a target's system, but never completes the handshake.
*   **Ping of Death:** A Ping of Death attack involves the attacker sending a malformed or oversized ping packet to the target.
*   **Smurf Attack:** A Smurf attack is a DDoS attack in which the attacker sends a large number of ICMP Echo Request packets with a spoofed source IP address to a network.

### 3. Application Layer Attacks

Application layer attacks, also known as Layer 7 attacks, are DDoS attacks that target the application layer of the OSI model. The goal of these attacks is to exhaust the resources of the target application. The magnitude of the attack is measured in requests per second (rps).

*   **HTTP Flood:** An HTTP flood is a DDoS attack that sends a large number of HTTP requests to a web server.
*   **Slowloris:** Slowloris is a DDoS attack that tries to keep as many connections to the target web server open for as long as possible.
*   **XML/JSON API Flood:** An XML/JSON API flood is a DDoS attack that sends a large number of XML or JSON requests to a web server.

## Mitigation

DDoS mitigation involves a set of techniques and tools for resisting or mitigating the impact of DDoS attacks. Some common mitigation techniques include:

*   **Rate Limiting:** Limiting the number of requests a server will accept from a particular IP address over a certain period of time.
*   **IP Blacklisting:** Blocking traffic from known malicious IP addresses.
*   **Content Delivery Network (CDN):** A CDN can help to absorb and mitigate the traffic from a DDoS attack.
*   **Web Application Firewall (WAF):** A WAF can help to filter out malicious traffic before it reaches the web server.