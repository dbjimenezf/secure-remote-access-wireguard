# Deployment

## Deployment Overview

The deployment phase consists of installing and configuring the VPN infrastructure according to the requirements and network design defined in the previous phases.

The implementation is based on Ubuntu Server and WireGuard, with individual configurations for authorized users.

The deployment process is divided into several stages to ensure that the VPN infrastructure is correctly configured and ready for testing.

## Server Preparation

The VPN service is hosted on an Ubuntu Server 24.04 LTS system.

The server provides the central infrastructure required to operate the WireGuard VPN service.

The deployment requires:

- Ubuntu Server 24.04 LTS.
- A server or virtual machine capable of hosting the VPN service.
- Stable network connectivity.
- Network access through the corporate router or firewall.

## WireGuard Installation

WireGuard is installed on the Ubuntu Server system as the VPN technology used by the infrastructure.

The installation provides the components required to create and manage VPN tunnels between the server and authorized remote clients.

## Server Configuration

After installing WireGuard, the VPN server is configured according to the network design.

The configuration includes:

- VPN network parameters.
- WireGuard service parameters.
- Authorized client configurations.
- Access control rules.
- Network and routing requirements.

The VPN network defined by the project is:

    10.0.0.0/24

The WireGuard service uses:

    UDP 51820

## Client Configuration

Each authorized remote user receives an individual WireGuard configuration.

The client configuration allows the user's device to establish a VPN connection with the central WireGuard server.

Supported client platforms include:

- Windows
- Linux
- Android
- iOS

Each client must be configured according to the access permissions assigned to the corresponding user.

## User and Key Management

The deployment includes the creation of users and the generation of the cryptographic keys required for WireGuard connections.

Each authorized client is configured as a WireGuard peer.

The configuration of individual peers allows access to be managed on a per-client basis.

Private keys and other sensitive configuration information must be kept protected and must not be included in the public repository.

## Access Rules

Network and access rules are configured to control communication between the VPN network and the internal corporate network.

The objective is to allow authorized VPN users to access the required internal resources while preventing unauthorized access.

The internal corporate network defined by the project is:

    192.168.1.0/24

## Initial Verification

After the server and clients have been configured, initial connectivity tests are performed.

The initial verification includes:

- Checking that the WireGuard service is operational.
- Establishing a VPN connection from an authorized client.
- Verifying connectivity through the VPN.
- Checking access to authorized internal resources.
- Verifying that the configured access permissions are applied correctly.

## Deployment Process

The complete deployment process can be summarized as follows:

```text
Ubuntu Server Preparation
          |
          v
WireGuard Installation
          |
          v
Server Configuration
          |
          v
User and Key Configuration
          |
          v
Client Configuration
          |
          v
Access Rules
          |
          v
Initial Connectivity Tests
