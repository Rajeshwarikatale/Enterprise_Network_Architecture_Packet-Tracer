Enterprise Network Design & Secure Routing Implementation (Cisco Packet Tracer)
Overview

This project demonstrates the design and implementation of a multi-router enterprise network using Cisco Packet Tracer. The network is structured to simulate a real-world organizational environment with segmented departments, routing across multiple networks, and secure remote management.

The focus of the project is on building a scalable network architecture using VLANs, IP subnetting, dynamic routing, and basic secure access configuration for network devices.

Network Architecture

The topology represents an enterprise-style hierarchical network with:

Multiple departmental VLANs
Layer 2 switches for access layer segmentation
Routers for inter-network communication
Point-to-point WAN links between routers using /30 subnets
End devices distributed across different VLANs

This structure reflects a simplified enterprise environment where each department operates within its own logical network.

VLAN Design

The network is segmented into multiple VLANs to improve organization and traffic management:

VLAN 10 – Sales
VLAN 20 – HR
VLAN 30 – Finance
VLAN 40 – Admin
VLAN 50 – ICT
VLAN 60 – Server Room

Each VLAN is mapped to specific switch access ports, ensuring proper separation of broadcast domains.

Trunk links between switches allow VLAN traffic to pass between network segments.

IP Addressing Scheme

A structured IPv4 addressing plan was implemented:

172.16.x.x private IP range for internal LANs
Subnetting used for department-level segmentation
/30 subnets used for router-to-router WAN links

This addressing strategy helps maintain scalability and logical separation of networks.

Inter-VLAN Communication

Inter-VLAN routing was implemented to enable communication between different departmental VLANs. This allows devices in separate VLANs to communicate through routing-enabled interfaces while maintaining segmentation at Layer 2.

Dynamic Routing (OSPF)

OSPF (Open Shortest Path First) was configured across multiple routers to enable dynamic route exchange within the network.

Key configurations include:

OSPF Process ID configured consistently across routers
Router IDs assigned manually for identification
Network advertisements configured for both LAN and WAN subnets
Area 0 used as the backbone area for routing exchange

This setup allows routers to learn and share network routes dynamically across the topology.

Secure Remote Access (SSH)

Secure remote management was configured on network devices using SSH.

Implemented security features include:

Domain name configuration for RSA key generation
Local user authentication setup
RSA key generation for encryption
SSH version 2 enabled for secure communication
VTY line configuration restricted to SSH-only access

This ensures encrypted remote access to network devices instead of unsecured Telnet-based management.

DHCP Configuration

Dynamic Host Configuration Protocol (DHCP) was used to automatically assign IP addresses to end devices within VLANs. This simplifies host configuration and reduces manual IP assignment errors.

Testing & Verification

Network functionality was validated using:

Ping tests between hosts across VLANs
Verification of DHCP IP allocation
Routing table inspection on routers
OSPF routing verification using CLI commands
Connectivity testing between multiple network segments

These tests confirmed successful communication between different parts of the network.

Key Learning Outcomes

This project helped develop practical understanding of:

VLAN segmentation and switch configuration
Inter-VLAN routing concepts
IP subnetting and network planning
Dynamic routing using OSPF
Secure device management using SSH
End-to-end troubleshooting in multi-router environments
Behavior of routing protocols in real network simulations
Tools & Technologies
Cisco Packet Tracer
Cisco IOS CLI
IPv4 networking concepts
OSPF dynamic routing protocol
SSH secure remote access protocol
Project Summary

This project represents a structured enterprise network simulation focusing on routing, segmentation, and secure access. It demonstrates practical networking implementation using Cisco Packet Tracer and reflects key concepts used in real-world network environments.

Future Enhancements
Implementation of multi-area OSPF
Addition of redundancy protocols (HSRP / EtherChannel)
Integration of ACL-based security policies
Expansion into IPv6 addressing
Improved network monitoring and logging simulation