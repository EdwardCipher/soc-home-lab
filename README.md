# soc-home-lab
SOC home lab with Wazuh SIEM, Sysmon telemetry, and Splunk-based SSH brute-force detection mapped to MITRE ATT&amp;C

SOC Home Lab – SIEM & Brute Force Detection

This project demonstrates a basic SOC home lab environment built for security monitoring and brute-force detection.

🧩 Architecture

Wazuh SIEM (All-in-One) on Linux

Windows endpoint with Sysmon and Wazuh Agent

Splunk Enterprise on separate Linux VM

SSH brute-force simulation and detection

Use Cases Implemented

SSH brute-force detection in Splunk

Field extraction for authentication logs

Successful login detection after brute-force

MITRE ATT&CK mapping in Wazuh

Real-time alert monitoring

Test Scenario

Simulated SSH failed logins

Observed alerts in Wazuh

Correlated events in Splunk
