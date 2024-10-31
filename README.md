# Large Critical Company Network Design and Simulation

## Overview
This repository contains a Cisco Packet Tracer lab that simulates a detailed network design for a large, critical company network. The design facilitates seamless interaction between departments across various buildings and locations, enabling secure and efficient data exchange. Cisco Packet Tracer (CPT) is used to create, test, and analyze this network, utilizing a range of network technologies to meet the company's connectivity, security, and operational requirements.

## Objectives
The objective of this lab is to build a robust network model for a large company, where multiple departments and office buildings are interconnected. The design prioritizes:
- Data exchange across locations with minimized latency.
- Optimized connectivity across both LAN and WAN networks.
- High security, availability, fault tolerance, and scalability.

## Case Study: Company Background
The **Computer & Construction Company (CCC)** was hired to establish a network for **BB Bank**, which includes:
- **Headquarters** located in Ho Chi Minh City.
- **Branches** in Da Nang and Hanoi.

### Key Design Requirements

#### Headquarters
1. **Building Structure**: 
   - The headquarters has 7 floors, with an IT room and Local Cable Center (LCC) on the first floor. The LCC uses a patch panel to organize cabling for structured management.
   
2. **Scale**:
   - The building houses approximately 120 workstations, 5 servers, and at least 12 network devices (routers, switches, security appliances, etc.).
   
3. **Network Technology**:
   - **Wired and Wireless Connectivity**: Wired Ethernet for primary devices and wireless access points for mobile devices.
   - **GPON Fiber Technology**: High-speed connectivity through GPON (Gigabit Passive Optical Network).
   - **GigaEthernet**: Using 1GbE/10GbE for critical, high-bandwidth connections.
   - **VLAN Architecture**: Each department is segmented with its own VLAN to isolate traffic and improve security.

4. **WAN and Internet Access**:
   - Two leased lines (SD-WAN or MPLS) connect the headquarters to branch offices. These lines handle internal WAN traffic.
   - Two xDSL connections for Internet access, configured with load balancing for optimized bandwidth utilization.
   - All Internet traffic is routed through the headquarters to maintain centralized security and monitoring.

5. **Software**:
   - A mix of proprietary and open-source software is utilized, covering office applications, client-server applications, multimedia applications, and databases.
   
6. **Security and Reliability**:
   - **Firewalls**: To protect the network from unauthorized access.
   - **IPS/IDS**: Intrusion Prevention and Detection Systems for real-time threat analysis.
   - **Phishing Detection**: Protection against phishing attacks to secure user data.
   - **High Availability (HA)**: Designed for minimal downtime, with redundant links and devices.
   - **Fault Tolerance**: Essential network components are configured for redundancy to withstand hardware or software failures.
   
7. **VPN Setup**:
   - **Site-to-Site VPN**: Establish secure connections with branch offices.
   - **Remote Access VPN**: Enables secure remote access for teleworkers to the internal company network.

8. **Surveillance**:
   - A **CCTV Camera System** is proposed to monitor activities within the headquarters. The cameras are centrally managed with a dedicated server for recording and access control.

#### Branches (Da Nang and Hanoi)
1. **Building Structure**:
   - Two-story buildings, each with an IT room and a Local Cable Center (LCC) on the first floor.
   
2. **Scale**:
   - Approximately 30 workstations, 3 servers, and 5 or more network devices per branch.

3. **WAN Connectivity**:
   - Both branches connect to the headquarters through WAN links, using SD-WAN or MPLS, depending on the cost-benefit analysis.
   - Available WAN options are analyzed based on cost, with pros and cons of each option documented for review.

### Data Traffic and System Load
- **Traffic Peak Hours**: Approximately 80% of network traffic occurs during peak hours (9-11 AM and 3-4 PM).
- **Data Transfer Requirements**:
   - **Servers**: Used for software updates, web access, and database queries. Expected daily download is ~1000 MB and upload ~2000 MB.
   - **Workstations**: Handle web browsing, document downloads, and customer transactions. Expected daily download is ~500 MB and upload ~100 MB.
   - **WiFi Devices**: Guest access devices mainly download content, with an average of ~500 MB/day.
- **Growth Forecast**: A projected 20% increase in users, network load, and branch expansion over the next five years.

## Technologies Used
This network design incorporates advanced technologies to maximize security, performance, and management capabilities, including:

1. **VPN**:
   - **Site-to-Site VPN**: Provides secure connections between the headquarters and branch offices.
   - **Remote Access VPN**: Facilitates secure, encrypted access for remote employees.

2. **Routing Protocols**:
   - **OSPF (Open Shortest Path First)**: A dynamic routing protocol used for efficient path determination across the network.

3. **Network Address Translation (NAT)**:
   - NAT is implemented for IP translation to manage and hide internal IP addresses when accessing external networks.

4. **Inter-VLAN Routing**:
   - Routing between VLANs allows segmented departments to communicate securely, preserving network segmentation.

5. **SSH (Secure Shell)**:
   - Securely accesses network devices for configuration and troubleshooting.

6. **LACP (Link Aggregation Control Protocol)**:
   - Link aggregation provides redundancy and load balancing across multiple connections for increased throughput and fault tolerance.

7. **Spanning Tree Protocol (STP)** and **BPDU Guard**:
   - STP and BPDU Guard prevent network loops and ensure smooth network operation.

8. **Surveillance System**:
   - **Security Cameras** with a central server for monitoring and recording are deployed, allowing for a robust surveillance solution.

## File Structure
- `Headquarters/`: Contains network configurations and VLAN setups specific to the headquarters.
- `Branches/`: Configurations and setups for Da Nang and Hanoi branch networks.
- `VPN_Configurations/`: Files related to site-to-site and remote access VPN setups.
- `OSPF_Configuration/`: OSPF settings for route optimization.
- `NAT_Settings/`: NAT configuration files for IP translation and routing.
- `Surveillance_System/`: Security camera system settings and management scripts.

## Setup Instructions
1. **Open the Cisco Packet Tracer File**:
   - Load the provided `.pkt` file in Cisco Packet Tracer.

2. **Verify VLAN Configurations**:
   - Check VLAN settings for each department in the headquarters and branches.
   
3. **Configure OSPF Routing**:
   - Ensure OSPF is configured correctly between all routers for optimal path selection.

4. **Test VPN Connections**:
   - Verify site-to-site VPN functionality between headquarters and branches.
   - Test remote access VPN for teleworkers.

5. **Monitor Surveillance System**:
   - Check the security camera feeds and central server to ensure operational readiness.

6. **Run Network Tests**:
   - Test network traffic during peak hours to evaluate load management and fault tolerance.
   - Use `ping`, `traceroute`, and other network diagnostic commands for validation.

## Future Enhancements
- **Expansion Capabilities**: Documentation and setup for scalability to support anticipated 20% network growth over the next five years.
- **Advanced Threat Detection**: Plans to incorporate advanced IDS/IPS and AI-driven threat analysis tools.
- **Automated Network Management**: Potential integration of automation tools for streamlined network monitoring and management.

---

