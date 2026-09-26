# Architecture

## Architecture Overview

The proposed architecture provides secure remote access to the company's internal network through a centralized WireGuard VPN server.

Remote users connect to the VPN through the Internet. The VPN traffic reaches the corporate network through the network perimeter and is handled by the WireGuard server.

The WireGuard server provides access to authorized users and connects the VPN environment with the internal corporate network.

## Main Components

### Remote Clients

Remote users connect to the corporate infrastructure using WireGuard client software.

Each authorized client has an individual VPN configuration.

Supported client platforms include:

- Windows
- Linux
- Android
- iOS

### Internet

The Internet provides the communication path between remote users and the corporate infrastructure.

Remote users can establish VPN connections from external networks to access authorized corporate resources.

### Router / Firewall

The router or firewall represents the network perimeter between the Internet and the corporate infrastructure.

It applies the required network and access rules for the VPN connection.

The WireGuard service uses UDP port `51820`.

### WireGuard Server

The WireGuard server is the central component of the VPN infrastructure.

It runs on Ubuntu Server 24.04 LTS and provides the VPN service for authorized clients.

Its main responsibilities include:

- Establishing VPN connections with authorized clients.
- Providing encrypted communication.
- Managing client configurations.
- Controlling VPN access.
- Providing connectivity between the VPN network and the internal network.

The VPN network uses the `10.0.0.0/24` address range.

### Internal Network

The internal corporate network contains the resources that remote users need to access.

The internal network uses the `192.168.1.0/24` address range.

Communication between the VPN environment and the internal network is controlled through the network configuration and access rules.

### Corporate Resources

Corporate resources represent the internal services and systems that authorized remote users may need to access.

These resources remain inside the corporate network instead of being directly exposed to the Internet.

## Network Flow

The general communication flow is:

1. A remote user connects using a WireGuard client.
2. The VPN connection travels through the Internet.
3. The connection reaches the corporate network through the router or firewall.
4. The traffic is handled by the WireGuard server.
5. The authorized client establishes a VPN connection with the server.
6. The VPN connection provides access to the VPN network.
7. Authorized traffic can reach resources within the internal corporate network.

## Network Segmentation

The architecture separates the VPN network from the internal corporate network.

### VPN Network

The VPN network uses:

    10.0.0.0/24

### Internal Network

The internal corporate network uses:

    192.168.1.0/24

The WireGuard server acts as the central component connecting the VPN environment with the internal corporate network.

## Logical Architecture

The logical architecture can be represented as follows:

    Remote Users
          |
          v
       Internet
          |
          v
    Router / Firewall
          |
          v
    WireGuard Server
      10.0.0.0/24
          |
          v
    Internal Network
      192.168.1.0/24
          |
          v
    Corporate Resources
