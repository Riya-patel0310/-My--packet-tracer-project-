




Site-to-Site IPsec VPN Configuration on Cisco ASA Firewall
 Overview

This project demonstrates the configuration of a Site-to-Site IPsec VPN using a Cisco ASA Firewall in Cisco Packet Tracer.

The VPN securely connects two separate networks over an untrusted/public network, allowing devices at both sites to communicate securely.

 Project Objectives
Configure Cisco ASA Firewall
Configure Site-to-Site IPsec VPN
Configure IKE Phase 1
Configure IPsec Phase 2
Configure pre-shared authentication
Configure encryption and hashing
Configure VPN traffic using access lists
Configure NAT exemption for VPN traffic
Verify VPN connectivity
Troubleshoot VPN connectivity problems
🖥️ Network Topology
LAN - Site A                         LAN - Site B

PC-A ── Switch ── Router ── ASA-A ═════ ASA-B ── Router ── Switch ── PC-B
                              │
                         Internet/WAN
                              │
                       Site-to-Site VPN
🔧 Technologies Used
Cisco ASA Firewall
Cisco Routers
Cisco Switches
Cisco Packet Tracer
IPsec VPN
IKE
ISAKMP
ACL
NAT
NAT Exemption
Pre-shared Key
AES Encryption
SHA Hashing
🌐 Example IP Addressing
Device	Interface	IP Address
Site A LAN	LAN	192.168.10.0/24
ASA-A Outside	WAN	203.0.113.1/30
ASA-A Inside	LAN	192.168.10.1/24
ASA-B Outside	WAN	203.0.113.2/30
ASA-B Inside	LAN	192.168.20.1/24
Site B LAN	LAN	192.168.20.0/24

Note: The IP addresses can be changed according to the topology used in the Packet Tracer project.

 VPN Configuration
IKE Phase 1

The VPN tunnel uses:

IKE/ISAKMP
Pre-shared key authentication
AES encryption
SHA hashing
Diffie-Hellman key exchange
IPsec Phase 2

IPsec is configured to provide secure communication between:

Site A LAN: 192.168.10.0/24
        ↕
   IPsec VPN Tunnel
        ↕
Site B LAN: 192.168.20.0/24
 Main Configuration Components
1. Interesting Traffic

An ACL is configured to identify traffic that should travel through the VPN tunnel.

Site A LAN → Site B LAN
2. NAT Exemption

VPN traffic is excluded from normal Internet NAT so that the original private IP addresses can be used across the tunnel.

3. IKE Policy

The IKE policy defines the security parameters used to establish the VPN tunnel.

4. IPsec Transform Set

The transform set defines how traffic is encrypted and authenticated.

5. Crypto Map

The crypto map connects the VPN policy to the outside interface of the ASA.

🧪 Verification

After configuration, the VPN can be verified using commands such as:

show crypto isakmp sa
show crypto ipsec sa
show crypto map
show access-list
show running-config
✅ Testing

The following tests are performed:

Ping from Site A PC to Site B PC.
Verify that the VPN tunnel is established.
Check IKE Security Association.
Check IPsec Security Association.
Verify encrypted and decrypted packet counters.
Troubleshoot connectivity if the tunnel does not establish.
🛠️ Troubleshooting

Common problems checked in this project include:

Incorrect IP addresses
Incorrect pre-shared key
Incorrect ACL
Incorrect crypto map
NAT interfering with VPN traffic
Incorrect IKE policy
Incorrect IPsec transform set
Missing routes
Interface shutdown
Incorrect VPN peer address
📂 Project Files
Site-to-Site-IPsec-VPN/
│
├── README.md
├── Site-to-Site-IPsec-VPN.pkt
└── screenshots/
    ├── topology.png
    ├── asa-configuration.png
    └── vpn-verification.png
📸 Screenshots

Add screenshots of:

Network topology
ASA configuration
VPN configuration
show crypto isakmp sa
show crypto ipsec sa
Successful ping between both sites
🏆 Skills Demonstrated

This project demonstrates practical knowledge of:

Cisco ASA Firewall
Network Security
Site-to-Site VPN
IPsec
IKE/ISAKMP
ACL
NAT
Network Troubleshooting
Cisco Packet Tracer
👨‍💻 Project Purpose

This project was created as a hands-on networking and cybersecurity lab to understand how two remote networks can communicate securely using a Site-to-Site IPsec VPN through Cisco ASA Firewalls.
