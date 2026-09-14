Cisco Packet Tracer Project #02 - VLAN & Trunking

Overview

A small office network is segmented into two VLANs: VLAN 10 (IT) and VLAN 20 (Finance). Two Cisco 2960 switches are connected through a trunk so both VLANs can cross one physical link.

1.  Objectives
    - Create VLAN 10 and VLAN 20.
    - Assign access ports.
    - Configure an inter-switch trunk.
    - Verify same-VLAN communication across switches.
    - Verify isolation between different VLANs.
    - Practice Cisco IOS verification and troubleshooting.

2.  Topology

    See topologi.png.
    Devices: 2 × Cisco 2960 switches, 10 × PCs.
    SW1: Fa0/1–Fa0/3 → VLAN 10; Fa0/4–Fa0/6 → VLAN 20; Fa0/24 → trunk.
    SW2: Fa0/1–Fa0/2 → VLAN 10; Fa0/3–Fa0/4 → VLAN 20; Fa0/24 → trunk.

3.  IP Addressing
    - VLAN 10: 192.168.10.0/24
    - VLAN 20: 192.168.20.0/24
    - Mask: 255.255.255.0
    - Gateway: not configured because this project intentionally has no Layer 3 routing.
      See addressing_table.xlsx.

4.  Core Configuration

        vlan 10
        name IT
        vlan 20
        name FINANCE

        interface range fa0/1-3
        switchport mode access
        switchport access vlan 10

        interface range fa0/4-6
        switchport mode access
        switchport access vlan 20

        interface fa0/24
        switchport mode trunk

    Apply the equivalent port assignments on SW2.

5.  Verification

    show vlan brief
    show interfaces trunk
    show interfaces status

6.  Testing

    Test | Expected
    PC-01 → PC-02 | Success
    PC-01 → PC-07 | Success — VLAN 10 across trunk
    PC-04 → PC-09 | Success — VLAN 20 across trunk
    PC-01 → PC-09 | Request timed out — VLAN isolation

7.  Technical Takeaway

    An access port carries one VLAN. A trunk can carry multiple VLANs between switches using VLAN tagging such as IEEE 802.1Q. A trunk does not perform routing; therefore VLAN 10 and VLAN 20 remain isolated until a Layer 3 device is introduced.

8.  Troubleshooting

    Check VLAN membership, trunk status, interface status, IP addressing, physical links, and VLAN existence on both switches.

9.  Next Project

    Project #03 — Inter-VLAN Routing / Router-on-a-Stick
