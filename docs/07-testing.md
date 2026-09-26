# Testing

## Testing Overview

Testing is required to verify that the VPN infrastructure operates correctly and that authorized users can securely access the corporate network.

The project defines several verification activities covering remote connectivity, encrypted communications, access permissions and the resolution of detected incidents.

## Testing Objectives

The main objectives of the testing phase are:

- Verify remote VPN connectivity.
- Verify that communications through the VPN are encrypted.
- Validate the access permissions assigned to users.
- Verify access to authorized internal resources.
- Identify and resolve connectivity or access issues.

## Connectivity Testing

The connectivity tests verify that an authorized remote client can establish a VPN connection with the WireGuard server.

### Expected Result

The authorized client should be able to establish the VPN connection and communicate through the VPN network.

The VPN network defined by the project is:

    10.0.0.0/24

## Encryption Testing

The encryption tests verify that communications between remote users and the corporate network are protected through the WireGuard VPN.

### Expected Result

Communication established through the VPN should use the encrypted WireGuard tunnel.

## Access Permission Testing

Access permission tests verify that users can access the resources assigned to them through the VPN.

### Expected Result

Authorized users should be able to access the resources permitted by the configured access rules.

Unauthorized access to restricted resources should not be permitted.

## Internal Resource Testing

Internal resource testing verifies connectivity between the VPN environment and the corporate internal network.

The internal network defined by the project is:

    192.168.1.0/24

### Expected Result

Authorized VPN users should be able to reach the internal resources that they are permitted to access.

## Incident Resolution

Testing also includes identifying and resolving connectivity or access problems detected during the verification process.

The troubleshooting process should include:

- Identifying the affected component.
- Checking the VPN connection.
- Reviewing the relevant configuration.
- Checking network and access rules.
- Applying the required correction.
- Repeating the relevant test.

## Test Summary

The following table summarizes the main tests defined for the project:

| Test | Objective | Expected Result |
|---|---|---|
| VPN Connectivity | Verify remote VPN access | Authorized client establishes a VPN connection |
| Encryption | Verify protected communication | VPN traffic is transmitted through the encrypted tunnel |
| Access Permissions | Validate user permissions | Authorized users can access permitted resources |
| Internal Resources | Verify internal network access | Authorized resources are reachable through the VPN |
| Incident Resolution | Verify troubleshooting process | Detected problems are identified and corrected |

## Test Evidence

Test evidence should be collected during the verification phase.

Examples of evidence include:

- WireGuard client connection status.
- Server VPN service status.
- Connectivity test results.
- Access to authorized internal resources.
- Screenshots showing successful VPN connections.

Test evidence should not contain private keys, passwords or other sensitive information.
