# Windows SOC Lab – Attack Simulation & Detection Project

## Objective
To simulate real-world attack techniques in a controlled lab environment and develop detection logic using Windows logs and Splunk SIEM.

---

## Lab Architecture

The lab environment consists of:

- Windows 11 Virtual Machine (Target + Log Source)
- Sysmon for enhanced logging
- Splunk SIEM for log ingestion and detection
- Kali Linux VM for attack simulation

### Network Configuration
- Host-Only network for isolated lab communication

### Architecture Diagram
                  ┌────────────────────┐
                  │   Kali Linux VM    │
                  │   (Attacker)       │
                  └─────────┬──────────┘
                            │ Attack Traffic
                            │
                            ▼
                  ┌────────────────────┐
                  │ Windows 10 VM      │
                  │ (Target / Log Source) │
                  │ - Sysmon Installed │
                  │ - Splunk Installed│
                  └─────────┬──────────┘
                            │ Logs Forwarded
                            ▼
                  ┌────────────────────┐
                  │ Splunk SIEM / Dashboards │
                  │ - Custom Alerts          │
                  │ - MITRE ATT&CK Mapping   │
                  └────────────────────┘


