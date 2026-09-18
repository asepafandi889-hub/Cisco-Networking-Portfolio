Cisco Packet Tracer Project #03 — Inter-VLAN Routing

Overview
This project demonstrates Inter-VLAN Routing using the Router-on-a-Stick method. VLAN 10 (IT) and VLAN 20 (Finance) use separate IP networks and communicate through router subinterfaces over an 802.1Q trunk.

Devices

- 1 × Cisco 2911 Router — R1
- 1 × Cisco 2960 Switch — SW1
- 6 × PCs

VLAN & IP Plan
| VLAN | Department | Network | Gateway |
|---|---|---|---|
| 10 | IT | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Finance | 192.168.20.0/24 | 192.168.20.1 |

Port Mapping

- SW1 Fa0/1–Fa0/3 → VLAN 10
- SW1 Fa0/4–Fa0/6 → VLAN 20
- SW1 Fa0/24 → 802.1Q trunk to R1 G0/0

Router-on-a-Stick

- R1 G0/0.10 → VLAN 10 → 192.168.10.1/24
- R1 G0/0.20 → VLAN 20 → 192.168.20.1/24
- R1 G0/0 enabled with `no shutdown`

Verification
SW1:

```text
show vlan brief
show interfaces trunk
show interfaces fa0/24 status
show interfaces fa0/24 switchport
```

R1:

show ip interface brief
show ip route

Testing
The completed project successfully achieved:

- Gateway connectivity from VLAN 10 and VLAN 20.
- Inter-VLAN communication between PC-01 (192.168.10.10) and PC-04 (192.168.20.10).
- 0% packet loss in the completed ping test.

Troubleshooting
Initially, SW1 Fa0/24 was configured as a trunk but showed `notconnect` and `Operational Mode: down`. The router-side G0/0 interface had not yet been activated. Enabling G0/0 with `no shutdown` brought the physical link up and allowed the trunk to operate.

Key Concepts
VLAN segmentation, access ports, 802.1Q trunking, Router-on-a-Stick, subinterfaces, default gateways, IPv4 addressing, Layer 2/Layer 3 routing, ICMP, and troubleshooting.

Outcome
The topology successfully routes traffic between VLAN 10 and VLAN 20 through R1, extending the Layer 2 VLAN concepts from Project #02 into Layer 3 Inter-VLAN Routing.
