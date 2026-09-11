



Inter-VLAN Routing + Multi-Area OSPF + DHCP Server
Project Overview

This project demonstrates the configuration and implementation of an enterprise-style network using Cisco Packet Tracer.

The network is designed to provide communication between multiple VLANs, dynamic IP address allocation using DHCP, and routing between different network areas using Multi-Area OSPF.

  Technologies & Protocols
  
VLAN
Inter-VLAN Routing
Trunking
DHCP Server
OSPF
Multi-Area OSPF
Cisco Routers
Cisco Switches
Cisco Packet Tracer
🎯 Project Objectives
Create and configure multiple VLANs.
Configure trunk links between network devices.
Enable communication between different VLANs.
Configure a DHCP server for automatic IP address assignment.
Configure OSPF for dynamic routing.
Implement Multi-Area OSPF using different OSPF areas.
Verify connectivity between different networks.
Troubleshoot routing and connectivity problems.
 Network Design

The project contains multiple VLANs and routed networks.

VLANs
VLAN	Purpose
VLAN 10	Department 1
VLAN 20	Department 2
VLAN 30	Department 3
VLAN 40	Department 4
Inter-VLAN Routing

Inter-VLAN routing allows devices in different VLANs to communicate with each other.

The router or Layer 3 switch provides the required Layer 3 gateways for the VLANs.

Example:

VLAN 10
   |
VLAN 20
   |
Inter-VLAN Routing
   |
VLAN 30
   |
VLAN 40
📡 DHCP

DHCP is configured to automatically provide IP configuration to end devices.

DHCP provides:

IP Address
Subnet Mask
Default Gateway
DNS Server

This eliminates the need to manually configure IP addresses on every PC.

🚦 Multi-Area OSPF

OSPF is used as the dynamic routing protocol.

The network is divided into multiple OSPF areas to demonstrate a scalable enterprise routing design.

Example:

             Area 0
               |
       ----------------
       |              |
    Area 1          Area 2
       |              |
    VLANs          VLANs

Area 0 is the OSPF backbone area, while other areas connect through the backbone.

🔧 Configuration Tasks
1. VLAN Configuration

Create VLANs on the switches:

VLAN 10
VLAN 20
VLAN 30
VLAN 40
2. Trunk Configuration

Configure trunk links between switches and the required network devices.

3. Inter-VLAN Routing

Configure Layer 3 gateways for each VLAN.

4. DHCP Configuration

Configure DHCP pools for the required VLAN networks.

5. OSPF Configuration

Configure OSPF and advertise the required networks in their respective areas.

6. Connectivity Testing

Verify connectivity using:

ping
traceroute
show ip route
show ip ospf neighbor
show ip ospf interface
 Verification

The following tests are performed:

PC receives an IP address from DHCP.
Devices within the same VLAN can communicate.
Devices in different VLANs can communicate.
OSPF neighbors are established.
OSPF routes appear in the routing table.
End-to-end connectivity between different networks is successful.



Project Files
Inter-VLAN-Routing-Multi-Area-OSPF-DHCP/
│
├── Inter-VLAN-Multi-Area-OSPF-DHCP.pkt
├── README.md
│
└── screenshots/
    ├── topology.png
    ├── vlan.png
    ├── dhcp.png
    ├── ospf-neighbor.png
    └── routing-table.png
 Software Used

Cisco Packet Tracer

 Learning Outcomes

Through this project, I practiced:

VLAN segmentation
Trunk configuration
Inter-VLAN communication
DHCP configuration
Dynamic routing
OSPF neighbor relationships
Multi-Area OSPF
Network troubleshooting
Connectivity verification

 Author

[Riya Patel]

Credits
This project was built while following a tutorial on YouTube: [video title or channel name] (add the link if you want)
