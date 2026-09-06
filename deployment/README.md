# Deployment

This directory contains the automation used to build and deploy the
Freshwater Treatment ICS Cyber Range.

The deployment layer combines Python, GNS3, Docker, and Jenkins to create a
repeatable industrial environment containing process PLCs, simulated
sensors, SCADA, HMI, historian services, field switches, an operations
network, and an authorized Kali Linux security workstation.

---

## Deployment Architecture

```text
GitHub
   │
   ▼
Jenkins
   │
   ├── Checkout repository
   ├── Build SCADA image
   ├── Publish container image
   ├── Build deployment image
   └── Run deployment
          │
          ▼
      GNS3 API
          │
          ├── Validate required templates
          ├── Register/update Docker templates
          ├── Create project
          ├── Create switches
          ├── Create PLCs
          ├── Create sensors
          ├── Create SCADA
          ├── Create HMI
          ├── Create historian
          ├── Create Kali
          ├── Configure interfaces
          ├── Configure node environments
          └── Create topology links
          │
          ▼
    Running Freshwater
       ICS Cyber Range
