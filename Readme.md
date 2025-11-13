Task 1 — Local Network Port Scan (Nmap)

Submitted by: Simanta Hazarika
Course: BTech CSE
University: Assam Kaziranga University

1. Objective

The objective of this task is to perform a local network scan using Nmap, identify active devices in the network, detect open ports, and understand the security risks associated with exposed services. This builds foundational skills in network enumeration and cybersecurity.

2. Tools Used

Kali Linux (VMware)

Nmap 7.94

Python SimpleHTTPServer (used to create a test open port)

3. Commands Used (Masked for Privacy)
3.1 Discover live hosts on the local network

sudo nmap -sn <local_subnet>/24 -oN ping_scan_masked.txt

3.2 Start a lightweight HTTP server on port 8080 (on Kali VM)

python3 -m http.server 8080

3.3 Scan the open port on localhost

sudo nmap -sS -sV -p 8080 localhost -oN kali_port8080.txt

4. Findings
4.1 Live Host Discovery

Nmap detected 7 active hosts on the network.

All IP and MAC addresses are masked.

Results saved in: ping_scan_masked.txt

4.2 Port 8080 Scan (localhost)

The open HTTP server on port 8080 was detected.

PORT STATE SERVICE VERSION
8080/tcp open http SimpleHTTPServer 0.6 (Python 3.11.9)

5. Security Analysis

Open ports increase the attack surface.

Port 8080 was opened intentionally for this task.

Phones/tablets had no open ports due to strong firewalls.

Router blocked external scans, which is normal.

Nmap identifies active devices, services, versions, and vulnerabilities.

6. Recommendations

Close unused ports.

Don’t expose test servers online.

Use firewalls (UFW/iptables).

Update services.

Disable unnecessary services.

Monitor unknown devices.

7. Files Included in This Repository

ping_scan_masked.txt
kali_port8080.txt
screenshots/
README.md

8. Conclusion

This task demonstrates host discovery, port scanning, service detection, and basic security analysis with Nmap. Opening and scanning a port provides real hands-on cybersecurity experience. This completes Task 1: Local Network Port Scan.
