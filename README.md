<p align="center">
  <img src="https://raw.githubusercontent.com/MauriceBurt/Modular-Networks/main/Transparent_PNG.png" width="350"/>
</p>

# Guest Wi-Fi Segmentation

This design demonstrates a foundational network segmentation model for a small business environment, focused on securing internal resources while providing controlled guest Wi-Fi access.

## Repository Structure

🔧 [Configs](./configs)  
🗺️ [Topology](./topology)  
📸 [Screenshots](./screenshots)

## Overview
This project simulates a retail-style network where guest users require internet access, but must be restricted from internal systems.

The network is segmented using VLANs to separate traffic between:

- Internal Network (VLAN 10)
- Guest Network (VLAN 20)

Inter-VLAN routing is handled using a router-on-a-stick configuration, with NAT and ACLs enforcing access control.

## Key Features
- VLAN-based segmentation (internal vs guest)
- Router-on-a-stick inter-VLAN routing (802.1Q)
- NAT (PAT) for internet access
- ACL enforcement to restrict guest access to internal network
- End-to-end validation using ICMP (ping)

## Network Behavior

Guest users are able to:
- Connect to Wi-Fi
- Receive IP addressing
- Reach the internet (via NAT)

Guest users are NOT able to:
- Access internal network resources

Internal users:
- Maintain full access to internal services
- Can reach external networks as needed

## Outcome

This design demonstrates a core security principle:

Even in small environments, segmentation is required to prevent unauthorized access.

It reflects a real-world baseline for businesses offering public Wi-Fi while protecting internal operations.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

## Screenshots

Key stages of the design and validation are included in the  
👉 [View Screenshots](./screenshots)

These include:

- Network topology
- VLAN configuration
- Trunking setup
- Inter-VLAN routing
- NAT configuration
- ACL enforcement (blocked vs allowed traffic)

## Configurations

👉 [View Configurations](./configs)

These configurations demonstrate:

- VLAN creation and assignment
- Trunk configuration
- Router subinterfaces (dot1Q)
- NAT (PAT) configuration
- ACL rules restricting guest access

## Topology File

👉 [Download Packet Tracer File](./topology)

Use this file to explore or replicate the full network design.
---
Part of the [Modular Networks Design Library](https://github.com/MauriceBurt/Modular-Networks).
