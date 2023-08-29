# Endpoint Security
## Table of Contents
1. Network & Endpoint Security Introduction
2. Problems & Risks
3. Endpoint Security Components
4. Endpoint Detection & Response
5. ClamAV Introduciton
6. YARA Rules & Signatures
7. Allow List Databases
## Network & Endpoint Security Introduction
- a suite of tools that helps protect workstations
- secures end-users devices ( desktops, laptops, etc.)
- Actively defends against risky activity and/or malicious attacks
- Operatoes as an enterprise security perimeter and is best suited for bring your own device ( BYOD )
## Endpoint Security Suite
![Alt text](<../assets/endpoint security suite.PNG>)
1. Antivirus - 
2. Data Loss Prevention ( DLP)
3. Application control/allow listing
4. Host Intrusion prevention/detection system ( HIPS/HIDS) , endpoint IPS/IDS
5. Communications Encrpytion
6. Email and Phishing protection
7. Logging and monitoring
8. Encrypted communication and hardware
## Antivirus Under the hood : Scanning
- Its from String/byte signatures
- hash signatures
- Heuristic detection
## Common Vendors
- Symantec Endpoint Protection
- Checkpoint Endpoint Security
- Kaspersky Endpoint Security
- McAfee Endpoint Protection
## Antivirus
- AV signatures must always be updated
- Designed to detect and remove viruses, trojans, worms, etc.
- Can quarantine or delete files
## Multi-engine antivirus scanning
- only one AV should be installed on a workstation.
- different avs, different methodologies and block lists, scanning w/ multiple engies simultaneously.
- multiple engines isnt talking about programs themselves, but its the actual platform where we are pulling the vulnerability data is from.
# ClamAV Introduction
- Open-source and cross-platform AV software
- mainly a CLI tool, although a GUI is available
- most features require initial configuration
## Pros & Cons
![Alt text](<../assets/ClamAV Pros & Cons.PNG>)
## ClamAV Configuration Files
- clamd.conf = ClamAV scan daemon settings
- freshclam.conf = change virus database update interval
- Clamconf = list both file configurations
# Problems & Risks
## False Positives & False Negatives
- False Positives = a test result falsely indicates the presence of a condition
- False negative = a test result mistakenly negates a condition
## False Positive ( F/P) Causes
- Heuristics = AVs evolve and so does viruses
- Behavioral Analysis = Legitmate apps behaving like malicious apps
- Machine Learning = Mistakes in training data fed to software
## Zero-Day
- a newly discovered flaw in a program
- exploited before a vendor can patch it
- Zero-day flaws are highly sought after by both hackers ( offense) and enterprise security teams (defense.)
## Antivirus Bypass Techniques
- Packing and Encryption
- Code Mutation
- Stealth Techniques
- Disable AV updates
- Fileless attack
# Endpoint Security Components
- Internal Firewall = Blocks incoming/outgoing connections to/from the workstation
- HIDS/HIPS = Detects, protects, and alerts upon malicious activity
- Sandbox = Restricted environment used to run suspicious programs and files.
## Device Control & BYOD
- expand the enterprise security perimeter
- employees connnect private devices to the company network
- potential of passing malware through company defense
    - BYOD = bring your own device
## Device Control & BYOD
- removable storage device
- policy enforcement
- data protection
# Endpoint Detection & Response
- Originally known as ETDR 
- Provides high visibility of endpoints
- Focuses on detecting and responding to malicious activity on the host
- Best use case: saerch manually for threats
## EDR vs. AV
- AV has a single purpose, detecting and removing malware
- EDR includes an AV
- EDR can protect against sophisticated threats ( advanced persistant threat APT) 
## Visibility & Response
- Securing endpoints requires real-time visibilty of all activites on the endpoint.
- Pinpoint malicious behavior
- Act swiftly to prevent an attack from becoming a breach.
# YARA Rules & Signatures
## Signature usuage
- AVs rely on signatures
- Vendors have different signature formats
- ClamAV Supports signatures written in YARA format
## Signature Types
- Body-Based Signature = Compares specific sequences of suspicious file bytes w/ malware models stored in a database
- Hash-Based Signature = Compares the file hash checksums of suspicious files w/ malware models stored in a database
    - Besides the signature types above, ClamAV allows the addition of custom signature files based on YARA rules.
## Writing a signature
- Sigtool is used to write and inspect signatures
1. the --md5 flag generates an MD5 hash.
2. Full file path
3. Output to test.hdb
![Alt text](<../assets/writing a signature.PNG>)
## Logical Signature
- Combines multiple signatures using logical operators
- enables more specific and flexible pattern matching
- File extensions include .ldb, .ldu, .idb
## YARA Rules
- a way of describing a pa ttern to identify files
- rules are written to meet specific conditions
- mainly used to classify particular strains or entire mmalware families.
## YARA Rule Structure
- the first part of the rule is its name
- Strings can specify text and hex values to search for.
- logical operators can be used in the condiiton of the rule.
![Alt text](<../assets/YARA Rule structure.PNG>)
## Yara Rule Signature
- ClamAV accepts YARA rules w/ certain limitations
- the extensions .yar and .yara are parsed as YARA rules
- maximum of 64 strings per rule
## PhishSigs
- Database of file signatures related to phishing
- file extensions:
    - .pbd = URLs of potential phishing sites
    - .gdb = URL hashes
    - .wdb = allow listed URLs
## Allow List DataBases
- AVs can mistakenly identify files as malicious
- ClamAV includes an option to allow listing applications
## Exclusions
- .fp = MD5 signature
- .sfp = SHA1 or SHA256 signature
- .ign2 = specific signature
    - These are allow list signature database file extensions
