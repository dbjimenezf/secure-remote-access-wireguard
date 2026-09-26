# Network Design

## Network Overview

The VPN infrastructure uses a dedicated VPN network to provide connectivity between remote users and the internal corporate network.

The network design separates VPN traffic from the internal corporate network while allowing controlled communication between the two environments through the WireGuard server.

## Network Addressing

The project defines two main network ranges:

| Network | Address Range | Purpose |
|---|---|---|
| VPN Network | `10.0.0.0/24` | Communication between the WireGuard server and VPN clients |
| Internal Network | `192.168.1.0/24` | Corporate internal network and resources |

## VPN Network

The VPN network uses the `10.0.0.0/24` address range.

This network is used by WireGuard to provide connectivity between the VPN server and authorized remote clients.

Each authorized client is assigned an address within the VPN network according to the WireGuard configuration.

## Internal Network

The internal corporate network uses the `192.168.1.0/24` address range.

This network represents the company's internal infrastructure and the resources that authorized remote users may need to access.

The internal network is not directly exposed to remote users through the Internet.

## WireGuard Service

The WireGuard VPN service uses UDP port `51820`.

The router or firewall must allow the required VPN traffic to reach the WireGuard server.

The WireGuard server acts as the central connection point between the VPN network and the internal corporate network.

## Traffic Flow

The general traffic flow between a remote user and an internal resource is:

```text
Remote Client
     |
     | WireGuard VPN
     | UDP 51820
     v
Internet
     |
     v
Router / Firewall
     |
     v
WireGuard Server
     |
     | Controlled routing
     v
Internal Network
     |
     v
Corporate Resources
