# 🛡️ Task 1: Scan Your Local Network for Open Ports

**Internship Program:** Elevate Labs Cyber Security Internship  
**Submitted By:** Mansi Raviya  
**Domain:** Cyber Security  
**Tools Used:** Nmap, Kali Linux  

---

## 📌 Objective
The main objective of this task is to perform network reconnaissance on the local network using **Nmap** to discover active hosts, identify open ports, and understand network exposure and security risks.

---

## 🛠️ Step-by-Step Implementation

### Step 1: Finding Local IP Address & Network Subnet Range
Before starting the port scan, we identified our system's network configuration and IP address using `ip a` and `ifconfig` commands on Kali Linux[cite: 2, 3].

* **IP Address:** `10.207.70.140`
* **Subnet Mask:** `255.255.255.0`
* **Target Network Subnet Range:** `10.207.70.0/24`

---

### Step 2: Running Nmap TCP SYN Scan
We performed a stealth TCP SYN scan (`-sS`) across the local network range (`10.207.70.0/24`) to detect active devices and open ports without completing the full 3-way TCP handshake.

```bash
sudo nmap -sS 10.207.70.0/24
