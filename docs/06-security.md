# Security

## Security Overview

Security is a central requirement of the VPN infrastructure.

The solution is designed to protect remote communications, restrict access to authorized users and reduce the risk of unauthorized access to the corporate network.

WireGuard provides encrypted communication between authorized VPN peers, while network and access rules control communication with internal resources.

## Encrypted Communications

The VPN uses WireGuard to establish encrypted tunnels between remote clients and the VPN server.

This protects data transmitted between remote users and the corporate network when accessing internal resources through the VPN.

The WireGuard service operates through UDP port `51820`.

## Authentication and Access Control

Access to the VPN is based on individually configured WireGuard peers.

Each authorized client has its own configuration and cryptographic keys.

This allows VPN access to be managed on an individual client basis and prevents unknown clients from being treated as authorized peers.

## Network Access Control

Access between the VPN network and the internal corporate network is controlled through network and firewall rules.

The objective is to allow authorized users to access the resources required for their work while limiting unauthorized communication.

The VPN network is:

    10.0.0.0/24

The internal corporate network is:

    192.168.1.0/24

## Protection of Sensitive Information

Sensitive configuration information must be protected throughout the deployment and maintenance of the VPN infrastructure.

Private keys and other confidential information must not be stored in the public repository.

Configuration examples included in the project should use placeholders instead of real private keys or other sensitive values.

## Security Testing

The project includes security-related verification activities such as:

- Verifying that VPN communications are encrypted.
- Checking connectivity from authorized clients.
- Validating user access permissions.
- Checking access to internal resources.
- Identifying and resolving connectivity or access issues.

## Security Maintenance

Maintaining the security of the VPN infrastructure requires regular review of:

- Authorized VPN clients.
- User access permissions.
- WireGuard configuration.
- Network and firewall rules.
- Server software and security updates.
- Backup procedures for relevant configuration information.

## Future Security Improvements

The original project identifies several possible improvements for future development:

- Multi-factor authentication (MFA).
- Advanced monitoring systems.
- Integration with directory services such as Active Directory.
- Automated backups of the VPN server configuration.

These improvements are considered future extensions and are not part of the current implementation scope.
