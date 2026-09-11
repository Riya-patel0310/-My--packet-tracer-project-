

Overview

This project demonstrates a multi-switch enterprise network built in Cisco Packet Tracer, featuring:

VLAN Segmentation — dividing the network across multiple access switches into separate VLANs

OSPF Routing — dynamic routing between two core routers for inter-network communication

Redundant Distribution Layer — two distribution switches (dSW1, dSW2) providing redundant links to access switches



The network consists of:

2 Routers (R1, R2) — each connected to a distribution switch via Gig0/0/0, on separate subnets (10.1.1.0/24 and 10.1.2.0/24)
2 Distribution Switches (dSW1, dSW2) — interconnected and cross-linked to all access switches for redundancy
4 Access Switches (ASW1–ASW4) — connecting end devices
8 PCs — distributed across the access switches
2 Servers — connected to ASW4
Key Configurations
VLAN Setup

Verification

Show output of commands like show ip route, show ip ospf neighbor, show vlan brief, or successful ping tests between PCs/VLANs.

Show output of commands like show ip route, show ip ospf neighbor, show vlan brief, or successful ping tests between PCs/VLANs.

Tools Used
Cisco Packet Tracer [version number]
Project File

The complete .pkt file is available in this repository under vlan-ospf-project/.
