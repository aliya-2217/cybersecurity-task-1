# 🔐 Cybersecurity Task 1 – Port Scanning using Nmap

This is Task 1 of my Cybersecurity Internship. The objective was to scan my local network for open ports using **Nmap** and optionally analyze the network traffic using **Wireshark**. This task demonstrates basic network reconnaissance skills and understanding of network exposure.

---

## 🛠 Tools Used

- **Nmap** – for network port scanning (`nmap -sS`)
- **Zenmap** – GUI frontend for Nmap 
- **Wireshark** – for packet capture and analysis 
- **Operating System** – windows 11

---

## 📡 Scan Details

### 🔍 Target Range
192.168.0.0/24

### 🧪 Command Used
```bash
nmap -sS 192.168.0.0/24

*Results Summary*
Hosts found: 4 live hosts
Open Ports per Host:

IP Address	                                      Open Ports (State)	                                  Service Name
192.168.0.1	                      22/tcp (open), 80/tcp (open), 1900/tcp (open),                  ssh, http, upnp, unknown
                                  49152/tcp (open)	                                              


192.168.0.1xx                    	53/tcp (filtered), 80/tcp (filtered),                           domain, http, msrpc, http-proxy
                                  135/tcp (filtered), 8080/tcp (filtered)	                       


192.168.0.1xx                    8008/tcp (open), 8009/tcp (open), 8443/tcp (open),              http, ajp13, https-alt, cslistener
                                  9000/tcp (open)	                                               


192.168.0.1xx                    135/tcp (open), 139/tcp (open), 445/tcp (open),                 msrpc, netbios-ssn, microsoft-ds, iss-realsecure,
                                  902/tcp (open), 912/tcp (open), 1521/tcp (open)	                apex-mesh, oracle 
                                                                                                  

*Screenshots*
All screenshots are in the screenshots/ folder:

✅ Nmap scan results

✅ Zenmap output 

✅ Wireshark packet capture

You can preview them directly in this repo.

*Security Observations*
-Several hosts have multiple open ports exposing various services such as SSH (22), HTTP (80, 8008, 8080), Oracle DB (1521), and Microsoft services (445).
-The presence of filtered ports (e.g., 53, 80 on 192.168.0.100) indicates firewall or filtering rules.
-Open ports increase the attack surface if services are vulnerable or misconfigured.
-Regular scanning and closing unused ports help reduce network exposure.

*Task Outcome*
This task helped me:
-Perform network reconnaissance with Nmap
-Understand TCP SYN scanning
-Visualize network traffic using Wireshark
-Identify open ports and their associated risks
