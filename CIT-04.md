# Mail Security
## Table of Contents
1. DNS Intro
2. Mail Protocols
3. DNS Mail Protection
4. Mail Headers
5. Mail Relay Intro
6. Mail Relay Concepts
7. Mail Relay Features
# DNS Intro
## What are DNS Records?
- Store information about every site on the web
- Before DNS, websites were accessed via host files
- DNS records tell DNS servers which domain is associated with which IP.
## Where is DNS Information Stored?
- The domain name registrar keeps track of domain names and IP assignments
- The domain name registry manages and maintains domain names
- Domains are not owned but reserved for a limited amount of time.
## DNS Queries
- A request for information from a client to a server
- MX records point to mail servers
- nslookup is used to query domain names and IP addresses.
## DNS Records
![Alt text](<../assets/DNS Records.png>)

# Mail Protocols
## Protocol Introduction
- SMTP ( Port 25 ) = Outgoing Mail
- POP3 ( Port 110) = Push mail
- IMAP ( Port 143) = Keep mail on Server
## How to connect via CLI
- connect and test a mail server via CLI
- **telnet < mail server name or IP> 25**
- **nc < mail server name or IP>25**
## Useful Commands for SMTP
![Alt text](<../assets/useful commands for smtp.png>)

## Useful commands for POP3
![Alt text](<../assets/Commands for POP3.png>)

# DNS Mail Protection
- Email Spoofing = Forging email headers to fool recipients into trusting the message
- DNS Spoofing = Creating fake DNS records to redirect traffic to a malicious website
    - Spoofing is a method of fabricating a valid-looking, but malicious service, device or network to perptrate an attack.
## SPF
- SPF = Sender Policy Framework
- Email authentication protocol
- SPF records store information about which IPs can send emails from a domain.
- Does not work when forwarding emails
## DKIM
- DKIM = DomainKeys Identified Mail
- Email validation technique
- Performed on the server level
- DKIM uses digital signatures
## DMARC
- DMARC = Domain-based message Authentication, reporting, and conformance
- The following DMARC policies can be used if an email fails a DMARC check: monitor, quarantine, reject.
- DMARC can generate a report about outgoing emails.
# Mail Headers
## What is an Email Header?
- Contains metadata for the email
- sender, recipient, content type, email route, authentication details, and more
- always precedes the message body
## How to find the Header
![Alt text](<../assets/how to find the header.png>)
## Important Header Fields
![Alt text](<../assets/Important header fields.png>)
# Mail Relay Intro
## What is Mail Relay?
- A server that routes emails to their correct destinations
- Email clients do not know how to send and deliver mail, they rely on mail relay
- provides a way to guarantee message authenticity
## Mail Relay Benefits
- Protect IP reputation
- Scan file attachments
- Spam, phising, and spoofing protection
## Topology Placement
![Alt text](<../assets/Topology placement.png>)
- a mail relay server can be placed either in the cloud or on a local network, and mail will be forwarded to it on the way to its destination.
## Mail Relay Concepts
## Mail Transfer Agent (MTA)
- The application side of mail servers
- Responsible for forwarding email to and from MUAs and other MTAs
- MTAs, Mail transfer agent, adds tags on top of message headers.
    - MUA = Mail User Agents
## Mail Delivery Agent ( MDA )
- sorting and delivery mechanism
- receives emails from MTA and delivers them to the recipient's inbox
- some MTAs can also act as MDAs
# Mail Relay Features
## Sandbox & File Extension Block List
- A mail relay sandbox provides a platform for testing email attachments.
- The sandbox scans the files behavior and checks it for indications of malicious intent.
- if it considers the file malicious, it drops the mail, and the recipient will not receive it.
    - blocking alone is not enough to prevent malicious files from being received.
## Antivirus & CDR
- Mail Server Antivirus = Scans incoming messages before tehy reach users and outgoing messages before they leave the computer
- CDR = Content Disarm & Reconstruction 
- Sanitizes files attached to emails.


