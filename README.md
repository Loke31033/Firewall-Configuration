# 🔒 Firewall Configuration Project (Kali Linux with UFW)

## 📌 Project Overview
This project demonstrates how to configure and test firewall rules on **Kali Linux** using **UFW (Uncomplicated Firewall)**.  
The goal is to understand how to list, add, block, allow, and remove firewall rules, as well as how firewalls filter network traffic.

---

## 🎯 Objectives
- Configure firewall rules on Kali Linux.  
- Block insecure ports (e.g., Telnet on port 23).  
- Allow secure access (e.g., SSH on port 22).  
- Test firewall functionality with networking tools.  
- Understand how firewalls improve security.  

---

## 🛠 Tools & Requirements
- **Operating System:** Kali Linux  
- **Firewall Tool:** UFW (Uncomplicated Firewall)  
- **Testing Tool:** Netcat (`nc`) or Telnet  
- **Privileges:** Root/sudo access  

---

## 🚀 Steps Performed

### Step 1: Install and enable UFW
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
Step 2: List current firewall rules
sudo ufw status numbered

Step 3: Block inbound traffic on port 23 (Telnet)
sudo ufw deny 23/tcp

Step 4: Test the rule
nc -vz localhost 23

Step 5: Allow SSH (port 22)
sudo ufw allow 22/tcp

Step 6: Remove the test block rule
sudo ufw status numbered
sudo ufw delete [rule_number]

📊 Observations

Port 23 (Telnet) was successfully blocked.

Port 22 (SSH) was allowed.

Firewall rules worked as expected.


📝 Conclusion

This project shows how UFW simplifies firewall management on Linux.
By blocking insecure ports and allowing secure ones, the firewall helps protect the system from unauthorized access and enhances overall network security.
