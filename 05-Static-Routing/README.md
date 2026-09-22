# Project 05 – Static Routing

## Project Overview

This project demonstrates the implementation of static routing using Cisco Packet Tracer.

The network consists of two separate local area networks connected through two Cisco routers. Static routes are configured on both routers to enable communication between the two different networks.

This project focuses on understanding basic routing concepts, routing tables, next-hop addresses, and end-to-end network connectivity.

---

## Objectives

The objectives of this project are:

- Understand the basic concept of IP routing.
- Configure IP addresses on router interfaces.
- Connect two different LAN networks using two routers.
- Configure static routes.
- Understand directly connected and static routes.
- Analyze routing tables using Cisco IOS commands.
- Verify connectivity between different networks.
- Perform basic routing troubleshooting.

---

## Network Topology

The network consists of:

- 2 × Cisco 2911 Routers
- 2 × Cisco 2960 Switches
- 4 × PCs

Network structure:

```text
PC-01 ──┐
        │
PC-02 ──┴── SW1 ── R1 ───── R2 ── SW2 ──┬── PC-03
                                         │
                                         └── PC-04
