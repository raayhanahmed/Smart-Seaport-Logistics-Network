# 🚢 Smart Seaport & Logistics Network Infrastructure

##  Project Overview

**Smart Seaport & Logistics Network Infrastructure** is an
enterprise-level network simulation developed in **Cisco Packet Tracer**
for a large seaport and logistics organization.

The project simulates a real-world port environment where multiple
departments, operational areas, servers, wireless users, CCTV systems,
and management networks communicate through a structured and scalable
network.

The network is designed around:

- Multiple departments and operational zones
- VLAN-based network segmentation
- IP subnetting
- Dynamic OSPF routing
- DHCP services
- DNS name resolution
- HTTP web hosting
- FTP file transfer
- Internal Email service
- NAT/PAT for Internet connectivity
- Wireless Access Points
- CCTV monitoring
- Separate server and management networks

------------------------------------------------------------------------

## Project Objectives

The main objectives of this project are to:

1.  Design a realistic enterprise network for a seaport.
2.  Connect multiple departments using routers and switches.
3.  Separate departments using VLANs.
4.  Apply subnetting for efficient IP address management.
5.  Implement OSPF for dynamic routing.
6.  Provide automatic IP addressing using DHCP.
7.  Configure DNS, HTTP, FTP, and Email services.
8.  Provide Internet access using NAT/PAT.
9.  Provide wireless connectivity for employees and guests.
10. Create a scalable network that can support future expansion.
11. Demonstrate practical Cisco networking concepts in a single Packet
    Tracer project.

------------------------------------------------------------------------

## Organization Structure

The simulated seaport contains the following major departments and
operational areas:

- Administration Department
- HR Department
- Finance Department
- Customs Department
- Shipping & Cargo Operations
- Warehouse Department
- Security & IT Department
- CCTV Monitoring Center
- Procurement Department
- Server Room / Data Center
- Office Wireless Network
- Warehouse Wireless Network
- Guest Wireless Network
- Management Wireless Network

------------------------------------------------------------------------

## VLAN & Network Segmentation

| VLAN | Department / Network | Network          |
|------|----------------------|------------------|
| 10   | Administration       | 192.168.10.0/24  |
| 20   | HR                   | 192.168.20.0/24  |
| 30   | Finance              | 192.168.30.0/24  |
| 40   | Customs              | 192.168.40.0/24  |
| 50   | Shipping / Cargo     | 192.168.50.0/24  |
| 60   | Warehouse            | 192.168.60.0/24  |
| 70   | Reserved             | 192.168.70.0/24  |
| 80   | Security & IT        | 192.168.80.0/24  |
| 90   | Reserved             | 192.168.90.0/24  |
| 100  | Server Room          | 192.168.100.0/24 |
| 110  | CCTV Monitoring      | 192.168.110.0/24 |
| 120  | Guest WiFi           | 192.168.120.0/24 |
| 130  | Procurement          | 192.168.130.0/24 |
| 140  | Office WiFi          | 192.168.140.0/24 |
| 150  | Warehouse WiFi       | 192.168.150.0/24 |
| 160  | Management WiFi      | 192.168.160.0/24 |

> **Note:** VLAN/IP values should be kept consistent with the `.pkt`
> configuration. If the topology is modified later, update this table
> accordingly.

------------------------------------------------------------------------

##  Routing Architecture

### OSPF Dynamic Routing

The project uses **OSPF (Open Shortest Path First)** as the main dynamic
routing protocol.

The network is divided into multiple logical OSPF areas to represent a
scalable enterprise environment.

Example design:

- **Area 0:** Backbone / Core Network
- **Area 1:** Administration, HR and Finance
- **Area 2:** Shipping, Cargo, Warehouse and Procurement
- **Area 3:** Security, IT, CCTV and Data Center

OSPF allows routers to dynamically exchange routing information and
select available paths between different network segments.

------------------------------------------------------------------------

## Router Architecture

The Packet Tracer topology contains a multi-router enterprise design
with:

- ISP / Internet Router
- Edge / Gateway Router
- Department / Building Routers
- Core Network
- Data Center Router

The uploaded topology contains **10 routers (R0–R9)**, providing a
larger WAN/core structure for the seaport environment.

------------------------------------------------------------------------

## Switching Infrastructure

The project uses:

- 1 Core Layer-3 Switch
- Multiple Access Switches
- Department-specific access switching
- Server Farm Switch

The Layer-3 core provides centralized connectivity between major network
segments and departments.

------------------------------------------------------------------------

##  Servers & Network Services

A dedicated **Server Room / Data Center** provides centralized network
services.

### DNS Server

Provides domain/name resolution for internal services.

Example:

``` text
www.smartport.com
ftp.smartport.com
mail.smartport.com
```

### DHCP Server

Provides automatic IP configuration to client devices and department
networks.

Typical DHCP information includes:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### HTTP Server

Hosts the organization’s web service.

Example:

``` text
http://www.smartport.com
```

Possible website sections:

- Home
- Port Information
- Cargo Operations
- Ship Schedule
- Contact
- Employee Services

### FTP Server

Used for transferring operational and cargo-related files.

Example folders:

``` text
Cargo/
Documents/
Reports/
Operations/
Backup/
```

### Email Server

Provides internal organizational communication.

Example accounts:

``` text
admin@smartport.com
hr@smartport.com
finance@smartport.com
cargo@smartport.com
customs@smartport.com
it@smartport.com
```

### Backup Server

A dedicated backup server can be used for storing important
configuration and operational data.

------------------------------------------------------------------------

##  NAT / Internet Connectivity

The network uses **NAT/PAT** to allow private internal networks to
communicate with the public Internet.

General flow:

``` text
Internal VLANs
      ↓
Private IP Network
      ↓
Edge Router
      ↓
NAT/PAT
      ↓
ISP Router
      ↓
Internet
```

This allows many internal devices to share public Internet connectivity
while keeping the internal addressing private.

------------------------------------------------------------------------

##  Wireless Network

The project includes multiple wireless networks.

### Office WiFi

Used by employees and office laptops.

### Warehouse WiFi

Used by warehouse staff and handheld operational devices.

### Guest WiFi

Used by visitors and guests.

### Management WiFi

Used by management-level users.

Wireless access points are connected to the appropriate network/VLAN to
maintain logical separation.

------------------------------------------------------------------------

##  CCTV Monitoring

A dedicated CCTV network is included.

### CCTV VLAN

``` text
VLAN 110
192.168.110.0/24
```

The CCTV environment contains:

- CCTV Cameras
- CCTV Monitoring PCs
- Dedicated Access Switch

This separates surveillance traffic from normal employee traffic.

------------------------------------------------------------------------

##  Client Device Scale

The topology is designed as a relatively large enterprise simulation and
includes approximately:

| Device              | Approximate Quantity |
|---------------------|----------------------|
| Routers             | 10                   |
| Core Layer-3 Switch | 1                    |
| Access Switches     | 12                   |
| PCs                 | 250+                 |
| Laptops             | 150+                 |
| Printers            | 35                   |
| Access Points       | 4                    |
| CCTV Cameras        | 20+                  |
| Handheld Devices    | 25+                  |
| Smartphones         | 90+                  |
| Servers             | 6                    |

The exact number of end devices can be expanded or reduced depending on
the academic requirements.

------------------------------------------------------------------------

##  High-Level Network Architecture

``` text
                         INTERNET
                             |
                         ISP ROUTER
                             |
                      EDGE / GATEWAY
                             |
                       CORE L3 SWITCH
             ________________|________________
            /        /       |       \         \
          R2       R3       R4       R5        R6
           |        |        |        |         |
      Admin/HR   Cargo   Warehouse  Customs   Security
           |        |        |        |         |
        Access    Access   Access   Access    Access
        Switch    Switch   Switch   Switch    Switch

                             |
                            R7
                       DATA CENTER
                             |
                      SERVER FARM SWITCH
             _____________|________________
            |       |       |       |       |
           DNS     DHCP    HTTP     FTP    EMAIL

                             |
                       Wireless / CCTV
```

------------------------------------------------------------------------

##  Network Security Considerations

The project can be extended with the following security mechanisms:

- VLAN segmentation
- Access Control Lists (ACL)
- SSH-based device management
- Port Security
- Strong device passwords
- Disabled unused switch ports
- Separate Guest VLAN
- Separate CCTV VLAN
- Separate Server VLAN
- Separate Management VLAN
- NAT/PAT for Internet access

These controls reduce unnecessary communication between unrelated
network segments.

------------------------------------------------------------------------

##  Testing & Verification

After configuration, the following tests should be performed.

### 1. VLAN Test

Verify that devices are assigned to the correct VLAN.

``` text
show vlan brief
```

### 2. Trunk Test

Verify trunk links.

``` text
show interfaces trunk
```

### 3. OSPF Test

Verify OSPF neighbours and learned routes.

``` text
show ip ospf neighbor
show ip route ospf
```

### 4. DHCP Test

Check whether client PCs automatically receive:

- IP address
- Subnet mask
- Gateway
- DNS server

### 5. DNS Test

Test hostname resolution:

``` text
ping www.smartport.com
```

### 6. HTTP Test

Open the server website from a client PC using:

``` text
http://www.smartport.com
```

### 7. FTP Test

Verify that clients can connect to the FTP server and transfer files.

### 8. Email Test

Send an email between two configured organizational accounts.

### 9. NAT Test

Verify that internal users can reach the external network through the
edge router.

### 10. Inter-VLAN Test

Verify communication between permitted VLANs.

------------------------------------------------------------------------

## 📁 Repository Structure

Recommended GitHub repository structure:

``` text
Smart-Seaport-Logistics-Network/
│
├── README.md
│
├── Packet-Tracer/
│   └── Smart-Seaport-Logistics-Network.pkt
│
├── Documentation/
│   ├── Network-Topology.png
│   ├── IP-Addressing-Table.pdf
│   └── Project-Report.pdf
│
├── Screenshots/
│   ├── Full-Topology.png
│   ├── VLAN-Configuration.png
│   ├── OSPF-Configuration.png
│   ├── DHCP-Server.png
│   ├── DNS-Server.png
│   ├── HTTP-Server.png
│   ├── FTP-Server.png
│   ├── Email-Server.png
│   └── NAT-Configuration.png
│
└── Configurations/
    ├── R0-Configuration.txt
    ├── R1-Configuration.txt
    ├── R2-Configuration.txt
    ├── R3-Configuration.txt
    ├── R4-Configuration.txt
    ├── R5-Configuration.txt
    ├── R6-Configuration.txt
    ├── R7-Configuration.txt
    ├── R8-Configuration.txt
    ├── R9-Configuration.txt
    └── Core-Switch-Configuration.txt
```

------------------------------------------------------------------------

##  Technologies & Tools

### Software

- Cisco Packet Tracer
- Git
- GitHub
- Visual Studio Code

### Networking Concepts

- IPv4
- Subnetting
- VLAN
- Inter-VLAN Routing
- OSPF
- DHCP
- DNS
- HTTP
- FTP
- Email
- NAT/PAT
- Wireless Networking
- Network Segmentation
- Basic Network Security

------------------------------------------------------------------------

##  Key Features

- ✅ Multi-department enterprise network
- ✅ Large-scale Cisco Packet Tracer topology
- ✅ 10-router architecture
- ✅ VLAN-based segmentation
- ✅ Subnetted IPv4 network
- ✅ OSPF dynamic routing
- ✅ DHCP
- ✅ DNS
- ✅ HTTP Web Server
- ✅ FTP File Server
- ✅ Email Server
- ✅ NAT/PAT Internet Access
- ✅ Wireless Access Points
- ✅ CCTV Network
- ✅ Management Network
- ✅ Guest Network
- ✅ Dedicated Server Farm
- ✅ Scalable architecture

------------------------------------------------------------------------

##  Academic Purpose

This project demonstrates practical implementation of enterprise
networking concepts in a simulated Smart Seaport environment.

It can be used for:

- Networking Lab Project
- Data Communication Project
- Cisco Packet Tracer Assignment
- Computer Networking Course
- Viva Demonstration
- GitHub Portfolio

------------------------------------------------------------------------

##  Future Improvements

The network can be expanded with:

- IPv6
- HSRP gateway redundancy
- EtherChannel
- Rapid STP
- DHCP Snooping
- Dynamic ARP Inspection
- AAA Authentication
- RADIUS
- Syslog
- NTP
- SNMP
- VPN
- Firewall
- Additional seaport branches
- Redundant Internet links
- High-availability server infrastructure

------------------------------------------------------------------------

##  Author

** Md. Abu Rayhan Ahmed **

Department of Computer Science & Engineering  
Daffodil International University

** Arpita Mondal **

Department of Computer Science & Engineering  
Daffodil International University

### Project

**Smart Seaport & Logistics Network Infrastructure**

------------------------------------------------------------------------

##  Disclaimer

This project is an academic network simulation created using Cisco
Packet Tracer. It represents a conceptual enterprise network and does
not represent the actual infrastructure or security configuration of any
real seaport.

------------------------------------------------------------------------

## Project Highlights

> **A scalable Cisco Packet Tracer enterprise network that integrates
> VLAN, subnetting, OSPF, DHCP, DNS, HTTP, FTP, Email, NAT, wireless
> networking, CCTV and multiple departments into one realistic Smart
> Seaport infrastructure.**
