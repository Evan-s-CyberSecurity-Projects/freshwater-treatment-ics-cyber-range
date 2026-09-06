# Security Policy

## Purpose

This repository contains an intentionally isolated educational
ICS/OT cybersecurity cyber range designed for authorized security
testing, research, and training.

The environment simulates a freshwater treatment facility using
GNS3, Docker, PLCs, SCADA, HMIs, industrial sensors, Modbus/TCP,
Jenkins, and Kali Linux.

Because the environment intentionally includes vulnerable and
security-testing components, care must be taken to ensure that
testing remains isolated from production systems and networks.

---

## Authorized Use

Security testing associated with this project is intended only for:

- The isolated GNS3 cyber range
- Locally controlled laboratory environments
- Systems for which explicit authorization has been provided

Do not use the techniques, configurations, or attack scenarios
demonstrated by this project against systems or networks without
authorization.

---

## Scope

The following components may be included within the cyber range:

- SCADA servers
- HMIs
- PLCs
- Simulated industrial sensors
- Modbus/TCP services
- Historian services
- Docker containers
- Jenkins deployment infrastructure
- GNS3 management interfaces
- Kali Linux security-testing systems

The cyber range is designed so that security activity can be
performed against these components without interacting with
production industrial infrastructure.

---

## Security Objectives

The project focuses on understanding and evaluating:

- Industrial asset exposure
- OT network segmentation
- Modbus/TCP security
- PLC security
- SCADA security
- HMI security
- Process-data integrity
- Availability risks
- Network reconnaissance
- Authentication and access control
- Container security
- CI/CD security
- Software supply-chain risks
- Security monitoring
- Anomaly detection
- Incident response

---

## Attack Simulation

Security exercises should be designed to demonstrate realistic
attack techniques while remaining controlled and reversible.

Examples include:

- Network and asset discovery
- Service enumeration
- Modbus/TCP enumeration
- Identification of PLCs and process roles
- Controlled register-access testing
- Simulated unauthorized control activity
- Process-anomaly generation
- SCADA/API security testing
- Jenkins and deployment-security analysis
- Container and image-security testing

Destructive actions against real-world infrastructure are outside
the scope of this project.

---

## Credentials and Secrets

Never commit the following to this repository:

- Passwords
- API tokens
- GitHub personal access tokens
- Jenkins credentials
- SSH private keys
- Docker registry credentials
- `.env` files containing secrets
- Production configuration
- Institutional credentials
- Sensitive network information

Use sanitized examples or environment variables when documenting
authentication or deployment configuration.

Example:

```text
GITHUB_TOKEN=<your-token>
JENKINS_URL=<your-jenkins-url>
DOCKER_REGISTRY=<your-registry>
