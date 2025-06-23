# Elevate Labs – Cyber Security Internship | Task 1 🔐

**This repository contains my work for **Task 1: Local Network Port Scanning** under the Elevate Labs Cyber Security Internship, supported by Skill India and Ministry of MSME, Govt. of India.
**
---

## 🎯 Task Objective

Perform a scan of the local network using **Nmap** to identify open ports and understand exposed services. This task helps in learning basic **network reconnaissance**, a critical part of ethical hacking and penetration testing.

---

## 📁 Files Included

| File Name                  | Description                                                  |
|----------------------------|--------------------------------------------------------------|
| `README.md`                | Overview of the task, steps followed, and learning outcome   |
| `nmap_scan.txt`            | Raw output from the Nmap TCP SYN scan                        |
| `ip_port_summary.md`       | Summary of active hosts, open ports, and associated services |
| `screenshot/scan_result.png| Screenshot of the Nmap scan result                           |

---

## 🛠 Tools Used

- **Nmap** for port scanning
- **Linux Terminal** – to run the commands
- **GitHub** for version control and documentation

---
## 🪜 Steps Followed


### 🔹 Step 1: Identifying Local IP Range

   Command used: ip a
   
           ## Output: 
            
         1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
             link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
             inet 127.0.0.1/8 scope host lo
                valid_lft forever preferred_lft forever
             inet6 ::1/128 scope host noprefixroute 
                valid_lft forever preferred_lft forever
         
                
         2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
             link/ether 00:0c:29:75:df:32 brd ff:ff:ff:ff:ff:ff
             inet 192.168.214.140/24 brd 192.168.214.255 scope global dynamic noprefixroute eth0
                valid_lft 1637sec preferred_lft 1637sec
             inet6 fe80::a973:4233:3029:3af4/64 scope link noprefixroute 
                valid_lft forever preferred_lft forever
         
         
         **Based on this, the scanned subnet is 192.168.214.0/24.
         **

                                                 
### 🔹 Step 2: Running Nmap TCP SYN Scan (This runs a stealth TCP SYN scan and saves the output)


            
              ## Command used: nmap -sS 192.168.214.0/24 -oN nmap_scan.txt
              
              ## Output: 
              
              Starting Nmap 7.95 ( https://nmap.org ) at 2025-06-23 05:06 EDT
            Nmap scan report for 192.168.214.2
            Host is up (0.00024s latency).
            Not shown: 999 closed tcp ports (reset)
            PORT   STATE SERVICE
            53/tcp open  domain
            MAC Address: 00:50:56:F4:27:77 (VMware)
            
            Nmap scan report for 192.168.214.254
            Host is up (0.00028s latency).
            All 1000 scanned ports on 192.168.214.254 are in closed states.
            Not shown: 1000 filtered tcp ports (no-response)
            MAC Address: 00:50:56:ED:A2:81 (VMware)
            
            Nmap scan report for 192.168.214.140
            Host is up (0.0000030s latency).
            All 1000 scanned ports on 192.168.214.140 are in closed states.
            Not shown: 1000 closed tcp ports (reset)
            
            Nmap done: 256 IP addresses (3 hosts up) scanned in 6.28 seconds




---
## 📸 Sample Scan Output

Screenshot of scan available in:  ![scan_result png](https://github.com/user-attachments/assets/4e98e882-09be-4c57-9d68-8f53213336c2)

---
## Summary 

  - 192.168.214.2 → Port 53/tcp (DNS) is open
  - 192.168.214.140 → All ports are closed
  - 192.168.214.254 → All ports filtered (probably a firewall/router)

## 🧠 What I Learned

- How to identify IP ranges and scan networks
- Use of `nmap -sS` (TCP SYN scan) to detect open ports using linux
- Interpreting port states and exposed services
- Recognizing common vulnerabilities associated with open ports
- Structured documentation of cybersecurity tasks






Thank you **Elevate Labs** for this opportunity to get real-world cybersecurity exposure.


