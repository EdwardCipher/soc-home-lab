# SOC Home Lab – Wazuh + Sysmon + Splunk

This project demonstrates a basic SOC home lab built for security monitoring and SSH brute-force detection.

The goal of this lab is to understand log collection, event analysis, and simple detection use cases.

---

## 🔧 Lab Components

- Wazuh SIEM (All-in-One) on Linux  
- Windows 10 endpoint with Sysmon  
- Splunk Enterprise on a separate Linux VM  

---

## 🏗️ Architecture

All machines are connected in the same virtual network.

### Log Flow

Sysmon → Wazuh Agent → Wazuh Server → Splunk

1. Sysmon collects Windows security telemetry  
2. Wazuh agent forwards logs to the Wazuh server  
3. Wazuh processes and stores the events  
4. Splunk is used for log searching and detection  

![Architecture](architecture.png)

---

## 🎯 Use Case – SSH Brute-Force Detection

This lab simulates an SSH brute-force attack and detects it using Splunk.

### Detection Logic

- Multiple failed SSH login attempts  
- Followed by a successful login  
- From the same source IP  

Mapped to:

MITRE ATT&CK  
T1110 – Brute Force  

---

## 🔍 What I Learned

- SIEM deployment and basic configuration  
- Windows event collection using Sysmon  
- Log forwarding with Wazuh agent  
- Searching and analyzing logs in Splunk  
- Creating a simple detection use case  

---

## 📸 Screenshots

Screenshots of the detection process are available in the `screenshots` folder.

### Wazuh Event Collection
![Wazuh](screenshots/wazuh-events.png)

### Brute-force Detection in Splunk
![Splunk Detection](screenshots/splunk-detection.png)

### Splunk Dashboard
![Splunk Dashboard](screenshots/splunk-dashboard.png)
---

## 🚀 Future Improvements

- Create a Splunk dashboard  
- Add alerting for brute-force detection  
- Add more attack scenarios  
