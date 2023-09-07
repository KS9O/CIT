# Honeypots

## Table of Contents
1. Introduction to Honeypots
2. Honeypot Strategy
3. Honeytokens
4. Honeytokens
5. Honeypot Products
6. Valhala Honeypots
7. Evasion
# Introduction to Honeypots
- Decoy devices meant to lure attackers ( such as APT)
- Service or OS Implementation
- Alarts are triggered when an attacker touches the trap.
## Honeypot Attributes
- Deliberately vulnerable information
- Logs the attacker's actions
- Identifies and defenders against APT
- Catches the bad guys in the act
## Honeypot Aims
- Analysis: Analyze the attacker's movement and gain insight into the attack
- Collection : Collect forensic data needed to improve security methods
- How do they work?
- simulate the behavior of a real system
- placed in accessible network areas
- have intentional security flaws
    - The security flaws may be a lack of security updates or unnecesarily enabled services.
# Honeypot Strategy
## Production Honeypots
- Emulate real production systems
- Emulate services or operating systems
- Learn the way attackers exploit vulnerabilities
- Minor or no false positives
# Research Honeypots
- Not meant for direct security value
- Can be used to research possible future threats
- Complex deployment and maintenance
- Not generally used by commerical organizations
    - The research helps gather information about a hacker's methods.
## Honeypot Interactions
- Low interaction : Provides limited access and covers specific ports and services, like home services
- High interaction : Emulates a complete sytem and monitors all performed actions.
- Honeypots are placed in locations with the highest potential of misleading an attacker.
# Honeytokens
## intro to honeytokens
- Fake IT resources
- Designed to attract the attackers attention
- typically found in public areas ( websites, documents, etc.)
    - Honeytokens may include hidden user credentials, email addresses, and fake webpages.
## Honeytoken Types
![Alt text](<../assets/honeytoken types.png>)
## Canary Traps
- Used to identify internal data leakers
- An almost identical copy of a document
- Leaked data is traced to the receiving person
    - Changes in the documents are tailored to the recipient. 
# Honeypot Products
## Commerical Honeypot Vendors
- Attivo ThreatDefend
- TrapX DeceptionGrid
- Acalvio ShadowPlex
## Open-Source Honeypot: Dionaea
- Open-source, low-interaction, server-side honeypot
- emulates complete vulnerable devices
- its main purpose is to make a copy of the malware.
## Open-Source Honeypot: HoneyDrive
- Virtual Xubuntu Desktop 20.04.4 appliance
- More than 10 pre-installed honeypot packages
- includes scripts and utilities 
## Modern Honey Network (MHN)
- MHN : Open-source platform for honeypot management, collects and analyzes honeypot data
- Quick Deployment: leverages existing open-source tools (Kippo, Suricata, etc.)
# Valhala Honeypot
- a honeypot that operates in Windows OS
- known for its ease of use
- supports various protocols, such as HTTP, FTP, Finger, SMTP, POP3, Telnet, etc.
## Valhala Features
- Medium-interaction type of a honeypot
- Easy to configure; no need to be an expert
- can include real files for a more authentic feel.
## Valhala config
- options = define the internal application settings
- Server Config = defines the honeypot services
- Verification will have green text for the active honeypot, make sure we remember; netstat -a
# Evasion
- knowing where the rap is - thats the first step in evading it. 
## Banner Grabbing
- Misconfigured honeypots = may reveal names and versions upon connections
- Banner grabbing = the banner grabbing method may reveal the honeypots existence
## Check the Uptime
- the uptime of a device may indicate it is a honeypot
- You can detect a honeypot by noting its exceptionally long or short uptime.
## Vendor Signature
- Many honeypots include well-known files.
- Kippo has a file called Kippo.cfg
- If an attacker discovers this file, the honeypot cover may be divulged.
## Enticing Vulnerabilities
- IF its too good to be true, dont believe it.
- lots of vulnerabilities
- a honeypots design should be as real as possible.
