# Monitoring

## Monitoring Overview

Monitoring is required to verify the availability, stability and correct operation of the VPN infrastructure after deployment.

The monitoring process focuses on the VPN service, connectivity, performance and security-related incidents.

## Monitoring Objectives

The main objectives are:

- Verify VPN service availability.
- Confirm that VPN connections can be established correctly.
- Monitor connection performance.
- Detect incidents that may affect the VPN service.
- Identify security-related incidents.
- Maintain records of relevant incidents and corrective actions.

## Key Indicators

The project defines the following quality indicators:

| Indicator | Purpose |
|---|---|
| VPN Connection Establishment | Verify that authorized clients can establish VPN connections |
| Service Availability | Verify that the VPN service remains available |
| Response Time | Identify abnormal delays during VPN connections |
| Security Incidents | Detect critical security-related incidents |
| User Satisfaction | Evaluate the experience of users accessing corporate resources remotely |

## VPN Service Monitoring

The WireGuard service should be periodically checked to verify that it is operating correctly.

The monitoring process should include:

- Service availability.
- VPN connection status.
- Authorized client connectivity.
- Connectivity with internal resources.
- Configuration changes affecting the VPN service.

## Connectivity Monitoring

Connectivity monitoring should verify communication between authorized VPN clients and the internal corporate network.

The VPN network is:

    10.0.0.0/24

The internal corporate network is:

    192.168.1.0/24

Connectivity problems should be investigated by reviewing the VPN configuration, network routing and access rules.

## Incident Management

VPN incidents should be registered and analyzed to determine their cause.

Possible incidents include:

- VPN connection failures.
- Loss of connectivity with internal resources.
- Incorrect access permissions.
- Service availability problems.
- Security-related incidents.

The incident management process should include:

1. Identification of the incident.
2. Registration of the incident.
3. Analysis of the possible cause.
4. Application of corrective actions.
5. Verification that the problem has been resolved.
6. Documentation of the resolution.

## Change Management

Changes to the VPN infrastructure should be documented to maintain traceability.

Changes may include:

- Adding new authorized users.
- Removing users.
- Modifying access permissions.
- Updating server components.
- Modifying network or firewall rules.
- Expanding the infrastructure.

Each relevant change should be documented together with its purpose and the actions performed.

## Monitoring Records

Relevant monitoring and incident information should be documented to provide a history of the infrastructure.

Records may include:

- Detected incidents.
- Corrective actions.
- Configuration changes.
- Test results.
- Availability issues.
- Security-related events.

This information can be used to evaluate the stability and reliability of the VPN infrastructure over time.
