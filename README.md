# DHCP and DNS Network Lab

Cisco Packet Tracer project demonstrating DHCP configuration DNS resolution IPv4 addressing and network connectivity.

## Project Overview

A small network was designed and configured using Cisco Packet Tracer.

The router provides DHCP services and acts as the default gateway while the server provides DNS services for the network.

## Network Topology

![Network Topology](DHCP-DNS-network-topology.png)

The network includes:

Router
Switch
4 PCs
DNS Server

## IP Addressing

| Device | IP Address      | Role                     |
| ------ | --------------- | ------------------------ |
| Router | `192.168.30.1`  | Default Gateway and DHCP |
| Server | `192.168.30.2`  | DNS Server               |
| PC0    | `192.168.30.11` | DHCP Client              |
| PC1    | `192.168.30.12` | DHCP Client              |
| PC2    | `192.168.30.13` | DHCP Client              |
| PC3    | `192.168.30.14` | DHCP Client              |

Subnet Mask: `255.255.255.0`

## Configuration

DHCP was configured on the router to automatically assign IPv4 addresses to the PCs.

The DNS server was configured with the domain:

`networklab.local`

The router interface was configured as the default gateway:

`192.168.30.1`

## Testing

### DHCP Configuration

![DHCP Configuration](DHCP-ipconfig.png)

DHCP was verified using `ipconfig`.

PC1 successfully received:

`192.168.30.12`

### Gateway Connectivity

![Gateway Test](Gateway-ping.png)

The connection between PC1 and the router was tested using:

`ping 192.168.30.1`

Result: **0% packet loss**

### DNS Resolution

![DNS Test](DNS-ping.png)

DNS resolution was tested using:

`ping networklab.local`

The domain successfully resolved to:

`192.168.30.2`

Result: **0% packet loss**

## Project Files

`DHCP-DNS-Network-Lab.pkt`

`commands.txt`

## Skills

Cisco Packet Tracer
DHCP
DNS
IPv4
Network Troubleshooting
Basic Network Configuration
