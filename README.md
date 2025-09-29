# Cyber Security Internship - Task 5  
**Task:** Capture and Analyze Network Traffic Using Wireshark  

---

## Objective  
To capture live network packets and identify at least three different protocols (e.g., TCP, DNS, HTTP) using Wireshark, and summarize the findings.  

---

## Environment  
- **OS:** Windows 10 (example – replace with your own)  
- **Tool:** Wireshark v4.x  
- **Interface:** Wi-Fi (active network interface)  
- **Capture Duration:** ~1 minute  

---

## Method  
1. Installed and launched Wireshark.  
2. Selected the active Wi-Fi interface.  
3. Generated traffic by browsing `www.google.com` and using `ping google.com`.  
4. Stopped the capture after ~60 seconds.  
5. Applied display filters (`dns`, `tcp`, `tls`) to analyze traffic.  
6. Identified multiple protocols.  
7. Exported the capture as a `.pcap` file.  

---

## Files Submitted  
- `network_capture_task5.pcap` → Raw packet capture file  
- `screenshots/` → Folder containing analysis screenshots (example: DNS query, TCP handshake, TLS Client Hello)  

---

## Protocols Identified  

1. **DNS (Domain Name System)**  
   - **Packet Example:** #12  
   - **Description:** Query for `www.google.com`, response from DNS server `8.8.8.8`.  
   - **Filter Used:** `dns`  

2. **TCP (Transmission Control Protocol)**  
   - **Packet Example:** #20–22  
   - **Description:** Observed TCP three-way handshake (SYN, SYN-ACK, ACK).  
   - **Filter Used:** `tcp`  

3. **TLS (Transport Layer Security)**  
   - **Packet Example:** #35  
   - **Description:** Client Hello sent to `google.com`. Payload encrypted.  
   - **Filter Used:** `tls`  

4. **ARP (Address Resolution Protocol)** *(optional extra)*  
   - **Packet Example:** #3  
   - **Description:** Request for gateway MAC address.  
   - **Filter Used:** `arp`  

---

## Observations  
- Majority of the traffic was encrypted TLS (HTTPS).  
- DNS queries were observed for resolving domain names.  
- TCP handshake confirmed connectivity establishment.  
- ARP packets showed local device-gateway communication.  

---

## Conclusion  
This exercise demonstrated how to capture and analyze live packets using Wireshark. I successfully identified **DNS, TCP, TLS, and ARP** traffic. The hands-on analysis improved understanding of how different protocols interact in real network communication. 
