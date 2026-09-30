# Lab 01 — Basic LAN

## Objective

Build, configure and troubleshoot a basic Local Area Network (LAN) consisting of two PCs connected through a Cisco switch.

## Topology

PC1 → Switch → PC2

## Devices

- 2 × PCs
- 1 × Cisco Catalyst 2960-24TT switch

## Configuration

| Device | IPv4 Address | Subnet Mask |
|---|---|---|
| PC1 | 192.168.1.10 | 255.255.255.0 |
| PC2 | 192.168.1.20 | 255.255.255.0 |

Both PCs were configured within the same IPv4 network, `192.168.1.0/24`.

Connectivity was tested using the `ping` command.

## Initial Problem

PC1 was unable to communicate with PC2.

The initial ping test resulted in 100% packet loss.

## Troubleshooting

I investigated the network configuration and identified two issues:

1. The FastEthernet0/2 switch interface was disabled.
2. PC2 had an incorrect IP address configuration.

I enabled the FastEthernet0/2 interface and corrected PC2's IP address.

## Verification

After correcting the configuration, I performed another ping test from PC1 to PC2.

The result was:

- Packets sent: 4
- Packets received: 4
- Packet loss: 0%

This confirmed that connectivity had been restored.

## What I Learned

- Devices communicating on the same subnet require compatible IP addressing.
- Hosts on the same network must have unique IP addresses.
- A disabled switch interface can prevent network connectivity.
- The `ping` command can be used to test basic IP connectivity.
- Network troubleshooting requires checking both endpoint configuration and network infrastructure.

## Skills Demonstrated

- IPv4 addressing
- Subnetting fundamentals
- Ethernet switching
- Basic Cisco Packet Tracer
- Connectivity testing
- Network troubleshooting
- Fault identification and resolution
## Evidence

### Working Network

![Working network and successful ping](Lab01%20working%20networking.png)

### Troubleshooting

![Network troubleshooting and failed ping](Lab01%20Troubleshooting%20network.png)
