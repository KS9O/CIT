# SIEM and SOAR
## Table of Contents
1. Alerts
2. Trends & Dashboards
3. SOAR Introduction
4. SOAR Capabilities
# Alerts
- Alerts are informative message, indicates a possible anomaly, threat or attack
- Its based on predefined criteria or rules.
    - Can be sent via email, SNMP, syslog, automatic scripts, or directly to situation management systems
## Alert Generation
- Monitor Events = Suspicious events in an organization trigger alerts that are handled by a security operations center ( SOC ) team.
- One or More Events = Alert-generating products have built-in alerts that have been tested in active systems.
## Types of Alerts
- Internal/External Attacks
- Compromised User Accounts and Workstations
- Abuse of Privileges
- Fraud
## Alert Flow
1. Log Inspection = Identify malicious activity from logs
2. Rule Definition = Create a rule to match the specific behavior.
3. Rule Testing = Verify that the rule matches the attack pattern
4. Fine Tuning = Reduce false positives by fine-tuning the alert.
5. Production = The alert is ready and waits to be triggered by an attack.
## Aggregation Alerts
- Consolidate logs w/ identical content in predefined fields and specific time frames
- Detect attacks like brute-force and port scanning
## Correlation Alerts
- Alerts from different events, correlated to a single result
- Indicate similar suspicious behavior among various system products
# Trends & Dashboards
## Anomaly Exploration
- Studies environment trends
- looks for any deviation from the norm
- Detects suspicious behavior
- uses a timeline to study behavior
## Real-Time Anomaly
- host=websrv source="/varlog/apache2/access.log" | bin_time span=5m | where code=403 or code 404 | stats count as Requests by _time | where Requests > 100
1. the host
2. the source
3. the sampled time span
4. searched parameter
5. statistics filter
6. condition
    - The query in the example above will display scanned logs of a website and report if the response was the 403 or 404 code more than 100 times, over a period of five minutes.
## Dashboards
- Various dashboards can be created in splunk
- granular dashboards configuration via SPL or XML
- Splunk has plugins for certain types of dashboards
## Event Dashboard
# Soar Introduction
- Designed to reduce the need for human intervention during IR
- Receives incidents from various systems ( not just SIEM )
- Executes automations as incident response functions
- Security Orchestration Automation and Response ( SOAR )
## How SOAR Works
- Like SIEM, SOAR receives events from multiple sources
- SOAR automates actions upon detection of specific events
    - a SOAR stack is a data structure that stores a collection of objects to improve security operation efficieny.
## SOAR Benefits
- Reduces response time to incidents
- Save time and money
# SOAR Capabilites
- **features**
- Security Incident Response = SOAR includes tools that respond to security-related incidents.
- Security Operation Automation = Repetitive tasks cn be automated to handle security incidents faster.
## Incident Case Management
- open and close cases w/o human intervention
- integrate w/ other case management systems
- some SOAR solutions use a ticketing method.
## Triage & Identification
- a way to identify and prioritize alerts
- SOAR triage is used in addition to the triage performed by the SIEM platform
- Solves the issue of what is considered critical
## Automation & Playbooks
- A flow of actions designed to reduce the need for human intervention in repetitive tasks
- Playbooks can be fully automatic or defined to require human intervention at critical decision-making points
- playbooks work w/ conditions for many types of scenarios.
