# Secure Network Architecture
## Table of Contents
1. Security Considerations
2. Concepts & Technologies
3. Disaster Recovery
4. Network Attacks & Mitigation
5. The Complete Picture
# Security Considerations
- Different topologies suit different needs
- Planned prior to the deployment of hardware
- Network architecture must be secured to compensate for the lack of TCP/IP safety.
## Network & Host Device Review
- Most devices that connect to a network are hosts.
- Host devices include computers, ioT and more.
- Node include hosts and intermediary devices
- The devices must have an IP address.
## TCP/IP Security
- TCP/IP was not designed w/ security in mind
- TCP/IP flaws fall into two categories
    - implementation flaws
    - protocol flaws
- both were addressed via new technology.
# Concepts & Technologies
## People, Processes, Technologies
- Security involces a blance among people, processes, and technologies.
- When appropriate processes are defined, people will be more effective in their tasks and technology wiill help them accomplish their tasks.
![Alt text](<../assets/people, processes, technologies.png>)
## Key Security Points
- Low Hanging Fruit = Easy targets for a hacker to pursue like unpatched or outdated software or firmware.
- Securing the weakest link = training eomployees for cyber awareness.
- the least privilege model = limit the damage that can result from an accident of free access permission.
## Patch Management
- Patch is a piece of code designed to improve an exisiting program.
- when a bug is discovered in a program, the vendor creates a patch to correct the issue.
- Proper patch management can prevent newly found vulnerabilities from being exploited.
# Secure Architecture Technologies
## Network Segmentation
- Divide a network into multiple segments or subnets.
- Prevent an attacker's lateral movement
- Employ zero-trust and use-trust assumptions
## Demilitarized Zone
- DMZ, also knwon as a perimeter network, is a physical or logiical subnet.
- placed between a LAN and a WAN.
- Designed to provide an additional layer of security.
## Network Access Control
- a method of controlling who has access to a network
- Access is based on rules
- Rules are enforced by policies
## Air-Gap Environemnt 
- Trusted networks should be physically isolated from unsecure networks.
- Prevent incoming and outgoing traffic from the internet.
    - Malware cannot connect to C&C
    - Malware cannot be downloaded directly via the internet
# Disaster Recovery
## Disaster and DR
- Disaster = damage caused to an organization's IT infrastructure
- Disaster Recovery = An organization's ability to recover and restore its IT infrastructure with the least impact on its business.
## Data Backup
- Data backup is the act of storing a copy of data in a separate storage location.
- a hot backup is taken from an up and running database.
- a cold backup is used when the database is offline.
## RAID
- a methodd in which several hard disks are combined into a single logical unit.
- RAID helps protect data by distributing it across multiple drives.
## RAID Types
- There are multiple levels of RAID
- Each level desribes an array of disks and how the data is stored across them
## Fault Tolerance
- An operation is sustained even if one or more componenets fail.
- To achieve fault tolerance, the remaining components must be able to run the system.
- Disaster recovery is based on fault tolerance.
    - An airplane w/ multiple engines is fault tolerant to partial engine failure.
## Failsafe Implementation
- Periodic backups are not enough
- neither are redundancies or failt tolerance
- a failsafe implementation means that all components work together to prevent or minimize damage in case of a disaster.
## Risk Assessment
- A document detailing potential risks and disasters
- Both natural and man-made disasters
- should be considered when building a DR plan.
# Network Attacks & Mitigation
- Active = Attacker attempts to change or steal data, typically comes after the reconnaissance phase.
- Phase = a system is monitored and scanned for open ports and vulnerabilities.
## Reconnaissance
- The phase in which information is collected to help decide which attack vector will be used.
- the chance of a successful attack can be determined by the quality of the reconnaissance.
## Passive Attacks & Mitigation
- Sniffing = Capturing data in transit between two points.
- Network-wide encryption will mitigate this tpye of attack. Sniffed data iis indecipherable.
- Phising = a seemingly legitimate email requests sensitive information.
- Email security and employee awareness training can mitigate this type of attack.
## Active Attacks & Mitigation
- DDoS = Large volumes of data sent from multiple sources to a single recipient
- backup and redundancies can minimize downtime in the event of a DDoS attack.
- Information theft and data breaches = Network segmentation and use of the least privilege model can minimize the damage.
# The Complete Picture
## Layered Security 
- Any single security measure may be flawed or insufficient.
- Layered security measures complement each other and together cover all the bases.
    - This is not the same as Defense in Depth ( DiD), which includes a broader strategic scope.
## Physicial Security Vs. Cybersecurity
- physical security is more intuitive than cybersecurity
- online protection is useless if anyone can easily access an office and the computers in it.
- physical security should bridge the gaps in network security.
## Summary
- There are standards, guidelines, and best practices for how to design a secure network architecture.
- the best defense is a layered approach that can bridge the gaps left by other security measures.
- a combination of physical security and network security will produce the most comprehensive framework.
