# Lab 04 — VLAN Segmentation

## Objective

Build a small business-style network using VLANs to logically separate different groups of devices on the same switching infrastructure.

## Requirements

- 2 VLANs
- 1 Cisco 2911 router
- 1 Cisco 2960-24TT switch
- 4 PCs

## Configuration

- VLAN 10
- VLAN 20
- Assigned appropriate switch ports to each VLAN
- Configured IP addressing for each VLAN
- Assigned at least 2 PCs to each VLAN

## Network Design

| VLAN | Network | Devices |
|---|---|---|
| VLAN 10 | 192.168.10.0/24 | PC1, PC2 |
| VLAN 20 | 192.168.20.0/24 | PC3, PC4 |

## Problem Encountered

PC1 could not communicate with PC2 because PC2 was assigned to the wrong VLAN.

## Troubleshooting

I identified that PC2 was assigned to VLAN 20 instead of VLAN 10. I assigned PC2 to the correct VLAN, VLAN 10, and then tested the connection again.

## Verification

PC1 successfully communicated with PC2 after PC2 was moved to VLAN 10.

## What I Learned

I learned that even a small configuration error on a networking device can prevent devices from communicating correctly. VLAN assignments determine which devices are logically grouped within a switched network, so the correct VLAN configuration is important for network connectivity and segmentation.

## Skills Demonstrated

- VLAN configuration
- VLAN segmentation
- IP addressing
- Ethernet switching
- Cisco Packet Tracer
- Network connectivity testing
- Network troubleshooting
- Fault identification and resolution

