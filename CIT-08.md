# lloT & ICS
## Table of Contents
1. Introduction to loT
2. Potential Risks
3. loT Security
4. Industrial Control Systems
5. Firmware
# Introduction to loT
- Internet of things
- devices that are connected to the internet
- everyday objects modified for the internet
## Where is loT Used?
- Consumer loT
- Agriculture & Meteorology
- Enterprise loT
- Industriial loT
    - loT offers the benefits of efficiency, safety, and improved quality of life through sensory feedback and automation.
## loT Usage
    - loT provides a way to control multiple smart devices from a phone or computer via apps.
![Alt text](<../assets/loT usage.png>)    
## How Does lloT Work?
- industriial internet of things
- sensors/devices
- data analysis and processing
- user interface
## lloT System Components
- Edge components = Manage all activities directly associated w/ the data source
- Smart Gateway = Connect edge components and the cloud or data center
- Connectors = the means by which collected data is sent to the gateway or cloud for processing
- Data proccessing = analyzing collected data and producing useful information based on the data
- User Interface = an interface through which users can manage sensors and make use of the data
## lloT Devices
- Traffic Lights
- Surveillance Cameras
- Engine and Machine Sensors
- Centrifuges
    - loT helps achieve automation via sensors and controllers
## Shodan
- The shodan search engine scans loT devices online using random IPv4 and port numbers
- it supports filters for granular searches
- paiid versions provide more detailed information for threat intelligence purposes
# Potential Risks
## Insufficient Security
- Lack of security awareness among developers
- lack of a macro perspective
- supply-chain-based security issues
- usage of unsecure frameworks and third-party libraries
    - there are cases in which a vendor may prefer efficiency over security.
## OWASP Top 10 loT Vulnerabilities
- Open Web application security project
- non-profit organization for web app security
- produce articles regarading web application vulnerabilites.
## loT Attack Vectors
- Device hardware
- web attacks on UI
- Unencrypted communicatiion
- firmware updates
## Common loT Attacks
- MiTM on unencrypted communication components
- DoS/DDoS on an loT device and using multiple loT devices as a botnet
- Replay attacks that replay authentication messages to deceive the destination server.
## The Fiver Layers of loT
- Perception
- Transmission
- Middleware
- Application
- Business
# loT Security
## Best Practice
- prior to moving to loT, research,invest, and plan for a secure loT infrastructure
- use VLANs and ACLs to segregate loT devices from the corporate network.
- Prevent loT devices from accessing the internet, unless it is crucial to their operation.
- Proper management of loT devices, limit vendor access to devices.
- Implement standard security measures on the loT system ( IPS, firewall, vulnerability scanner, NAC).
- Remove end-of-life (EOL) and deprecated devices, applications, and OS's from the network
## Smart City Security
- A city-scale operation involves many new challenges
- New technology meets legacy technology
- an attack on such systems may be critical
# Industrial Control Systems (ICS)
- Systems that monitor and manage industrial machinery
- Integrate hardware, software, and network.
- Maintain remote support and management of critical infrastructure.
## Industrial Applications of loT
- Automate teime-consuming tasks to increase efficiiency and reduce busywork.
- Remote asset moniitoring and deployment of loT in challengiing environments
- Predictive maintenance for safety and cost efficiency.
## ICS Components
- Supervisory Control and Data Acquistion (SCADA)
- Human-Machine Interface (HMI)
- Programmable Logic Controllers (PLC)
- Remote Terminal Units (RTU)
## ICS Protocols
- RS-485 and Modbus are examples of ICS protocols
- Some protocols were designed for systems that do not have internet connectivity.
# Firmware
- Semi-permanent software for hardware
- written on dedicated board flash memory
- Intrsucts devices on how to communicate w/ other hardware and software
    - Firmware updates are not as frequent as software updates.
## Where does firmware reside?
- Routers
- Computers
- Washing Machines
- Televisions
    - Most eletriconic devices contain firmware
## Attacking Firmware
- Why? = Firmware breaches provide high-level privileges, stronger persistence, and better chances of bypassing security controls
- How? = Software down, such as exploiting a lack of updates and patches
- Hardware up, such as injecting malicious firmware via a USB device
    - Firmware can be breached to allow attackers to access systems, often without the owner knowing about it.
## Obtaining Firmware
- Download from Vendors
- Dump from Device
- Sniiff over the Air (OTA)
- Reverse Engineering
    - OpenWrt is a website that provides home router firmware.
## Embedded Fiile Systems
- SquashFS
- Cramfs
- JFFs2
- YAFFS2
- ext2
## Information Gathering
- As much information as possible should be gathered about firmware to ensure in-depth analysis.
- Entropy measures the randomness of data to cehck for compression or encryption.
- Firmware can be encrypted. XOR and AES are commonly used.
## Hard-Coded Secrets
1. Sensitive URLs
2. Encryption algorithm
3. Authentication and authorization mechanisms
- Access Tokens
5. Hard-coded credentials
6. Local pathnames
7. Environment details
8. API and encryption keys
## Common Tools
- DD
- HexDump
- Strings
- Binwalk
- qemu 