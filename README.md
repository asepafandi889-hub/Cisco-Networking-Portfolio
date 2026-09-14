Cisco Packet Tracer Project #01 - Basic Office LAN

1. Project Overview
   This project simulates a small office Local Area Network (LAN) using Cisco Packet Tracer. The network consists of one Cisco 2960 switch and four PCs connected through Ethernet.
2. Objective
   - Understand the basic concept of a LAN.
   - Configure static IPv4 addresses.
   - Understand the role of a Layer 2 switch.
   - Test connectivity using ICMP ping.
   - Observe ARP and the relationship between IPv4 addresses and MAC addresses.
   - Practice basic network troubleshooting.
3. Topologi
   - 1 × Cisco 2960 Switch (SW1)
   - 4 × PCs (PC-01 to PC-04)
   - Copper Straight-Through Ethernet cables

4. IP Addressing
   Network: 192.168.1.0/24
   Subnet Mask: 255.255.255.0

   Device IP Address
   PC-01 192.168.1.10
   PC-02 192.168.1.11
   PC-03 192.168.1.12
   PC-04 192.168.1.13

   Default gateway is intentionally left empty because all hosts are in the same subnet and no router is used.

5. Port Mapping

   Device Switch Port
   PC-01 SW1 Fa0/1
   PC-02 SW1 Fa0/2
   PC-03 SW1 Fa0/3
   PC-04 SW1 Fa0/4

6. Testing
   Connectivity is tested with : ping 192.168.1.x
   ARP can be inspected with : arp -a
   Local IP configuration can be inspected with : ipconfig
7. Key Concepts
   IPv4 Address identifies a device at the network layer
   MAC Address identifies a network interface at the data-link layer
   ARP (Address Resolution Protocol) maps a known IPv4 address to a MAC address on the local network
   Switch forwards Ethernet frames based on MAC-address
8. Troubleshooting Exercise
   A useful practice is to intentionally change PC-04 to a different subnet, test connectivity, and then diagnose the problem using:
   - ipconfig
   - ping
   - arp -a
   - Physical/link status
   - IP and subnet verification
9. Expected Outcome
   All four PCs should be able to communicate with each other because they belong to the same IPv4 subnet and are connected through the same Layer 2 switch.
10. Skill Demonstrated
    - Basic LAN design
    - IPv4 addressing
    - Subnetting fundamentals
    - Ethernet switching fundamentals
    - ARP
    - ICMP ping
    - Basic troubleshooting
    - Cisco Packet Tracer
