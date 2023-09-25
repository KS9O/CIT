# Data Loss Prevention
## Table of Contents
1. Sensitive Data
2. Data Leak Channels
3. Regular Expressions
4. DLP Introduction
5. OpenDLP
6. DLP Bypass Techniques
# Sensitive Data
![Alt text](<../assets/data classification.png>)
## Data Types
- Personal Data
- Customer Data
- Intellectual Property
- Financial Data
## Personal Identity Information
- Health Information
- Race/Ethnic Origin
- Political Opinion
- Religious or Philosophical Beliefs
## Internet Data
- Cookie IDs = A value used by web servers and browsers for authentication and session recognition
- Hashed Email Addresses = Maintain recognition w/ identity privacy
- Mobile Advertising IDs = A replacement for cookies in mobile app environments
# Data Leak Channels
## Phyiscal Components
- Information can be leaked by employees or stolen by cyberthieves.
- USB ports should be locked down, and portable device disks should be fully encrypted.
- Webcams, network printers, and guest Wi-Fi should be secured and segmented.
## Network
- Sharing Websites are typically permitted on company networks.
- Full TLS inspection is not enabled on many sites.
- Web Filtering is often not strict enough.
    - TLS inspection is a method in which TLS traffic is decrypted and inspected.
## Malware
- Multi-staged malware can be crafted by a variety of tools
- Social media can be used to trigger payloads of dormant malware
- New payloads are not uploaded to online scanners because they send new signatures to AV vendors.
## Protocol Abuse
- DNS Tunneling = Embedding encrypted chunks of data in DNS queries
- File Server Traffic = protocol like SFTP is permitted in outbound traffic
- ICMP Tunneling = Sending data using echo packets
## Regular Expressions
**What is Regex?**
- a method used to describe a specific pattern of characters
- Highly flexible, w/ customizable search parameters
- Text processing tools PowerGREP enable easier query crafting.
## Regex uses
- searches for text and replaces text
- Text input validation
- Less code that does more work
## Regex for DLP
- Filter outbound emails to look for:
- Credit card numbers
- Social Security information
- custom dicitonary phrases
- specific data types
## Syntax Patterns
![Alt text](<../assets/syntax Patterns.png>)
## IP Simple Regex Example
![Alt text](<../assets/IP Simple Regex Example.png>)
1. \d represents a digit
2. {1,3} a group of one to three consecutive numbers ( such as 242)
3. \ . Dot denotes a special character and is escaped with \
    - This pattern isn't perfect. For example, the number 823 can be in either of the groups. (IP octets can be from 0-255.)
# DLP Introduction
## DLP Purpose
- Prevents organizational data from being shared w/ unauthorized parties
- Prevents both intentional and unintentional data loss
- Compliance w/ privacy laws and regulations
## How DLP Works
- Content inspection and contextual analysis
- Based on Rules and policies
- uses regex pattern matching
## Local Agent Protection
- Monitor and block the printing of confidential material
- Review the clipboard and block the copying of sensitive content
- analyze and block email messages sent to specific destinations.
## Block List vs. Allow List
![Alt text](<../assets/block list vs allow list.png>)
# OpenDLP
- OpenDLP is a free,open source, multi-platform, centrally managed, and highly distributable, agent-based or agentless, able to concurrently scan thousands of OS's.
- OpenDLP uses agents for web applications and windows machines, agentless database scans, and agentless file system and file share scan.
