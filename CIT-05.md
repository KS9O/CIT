# SIEM Introduction
## Table of Contents
1. Security Measures
2. Introduction to SIEM
3. SIEM Installation
4. Log Collection & Types
# Security Measures
## Cybersecurity Threats
- Threat
- Vulnerability
- Risk
- Asset
## Technological Asset Types
- Hardware
- Software
- Data
- Communications
    - Each of these assets can be an attack vector and must be monitored continuously.
## Security Components
1. Network Access Control
2. Network Behavior Analysis
3. Firewall
4. Identity Management
5. Web Application Firewall
6. Virtual Private Network
7. Intrusion Detection and Prevention
8. Endpoint Detection and Response
9. Mail Relay
10. Endpoint Protection Security
## SOC vs. NOC
- -**SOC**-
-  Security Operations Centers ( SOCs) manage security incidents
- Help monitor logs from different systems and respond to incidents
- Personnel handle data analysis and technologies
- Use SIEM and ticket management
- -**NOC**-
- Network Operations Centers (NOCs) manage network operatiions
- A central location for controlling and monitoring network components
- Personnel handle network management, configuration, and IT.
- Use control systems, quality management, and tracking tools
# Introduction to SIEM
## SIEM for Security
- Log collection software and log retention
- Security incident alarts based on logs
- Provides data analysis
    - Some organizations use SIEM as a third-party service to monitor infrastructure.
## Why SIEM is Important?
- Helps detect security incidents at an early stage
- Creates reports of suspicious activites
## SIM, SEM & SIEM
![Alt text](<../assets/SIM, SEM & SIEM.png>)
## SIEM General Components
- Database
- Correlation Engine
- Collectors
- Management Center and Dashboards
- API 
## SIEM Monitoring Features
- Filters
- Rules
- Active Lists
- Reports
- Trends
## Siem Workflow
- 1. Collection = gathers logs and data-related events.
- 2. Parsing = Inspect the data and sort it into key and value pairs
- 3. Evaluation = Match against sets of rules to indicate a threat
- 4. Correlation = Note if suspicious behavior is part of a more elaborate scenario.
- 5. Inspection = Tickets are managed by the SOC.
## SIEM Key Objectives
- Near-real-time alerts and correlations
- Conduct investigations and provide evidence
- Provide risk management and assessment for corporate assets.
## Popular SIEM
- QRadar
- ArcSight
- AlienVault
- Splunk
## snort
- an open-source IDS/IPS system
- Can perform real-time network traffic analysis
- supported by pfSense
# SIEM Installation
## Splunk Components
- Search Head is an interface used to search and access data.
- indexedrs are the log parsers.
- small components collect data to be sent to splunk.
## Splunk Installation in Linux
![Alt text](<../assets/Splunk installation in Linux.png>)
## Installation in Windows
- The splunk windows installation follows steps that are similar to a Linux installation
- Credentials for the system are provided during the installation process
- splunk forwarder should be iinstalled separately ( on Linux, Windows, or Mac).
## Splunk Plugins
- Add-on = Typically a single component that can be reused in different use cases
- Apps = More comprehensive and may contain user interfaces
    - Apps and add-ons extend Splunk functionality.
# Log Collection & Types
## Log Structure
![Alt text](<../assets/Log Structure.png>)
## log Collector
- Typically located in every environment
- collectors forward logs received from OSs and applications to the SIEM.
- To send logs from DMZ to LAN, specific ports must be opened.
![Alt text](<../assets/Log Collector.png>)
## Application Logs
- DB
- WAF
- IPS
- FIREWALL
    - Logs can also be obtained through external applications.
## OS Logs
- UNIX systems usually save logs in the /var/log directory
- in Windows, logs can be viewed in the event viewer
- Macs uses console.app, which is similar to the windows event viewer.
## UNIX Logs
![Alt text](<../assets/UNIX Logs.png>)
## UNIX Log Sources
- Auth.log
- Apache2
- IPtables
- Syslog
- DPKG
## Windows Event Logs
![Alt text](<../assets/Windows Event Logs.png>)
- Application
- Security
- Setup
- System
- Forwarded Events
## Important Security Events
    - Windows events are assigned IDs.
- 4624 = Successful user login
- 4625 = Failed user login
- 4672 = Special privileges were assigned to a new logged on user.
- 4700 = Scheduled task was enabled.
- 1116 = Windows Defender malware detection
- 5031 = A firewall service blocked an application from accepting incoming connections.
## Event Log Classification
- Information Logs
- Warnings
- Error Logs
- Success Audit
- Failure Audit
![Alt text](<../assets/Event log Classifications.png>)
## Log Gathering
- Syslog can use TCP/UDP when the default port is 514.
- Files = Some applications use files to write logs
- Database = SIEM logs in to the database and extracts logs according to a predefined query.

## Do challenge Events are Important
