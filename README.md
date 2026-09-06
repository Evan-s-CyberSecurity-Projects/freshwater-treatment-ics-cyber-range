# Freshwater Treatment ICS Cyber Range

> A reproducible industrial control system (ICS) and operational technology (OT) cyber range modeling a freshwater treatment facility for cybersecurity training, attack simulation, monitoring, and incident-response exercises.
The project combines industrial process simulation, network segmentation, automated infrastructure deployment, operator visualization, and authorized security testing into a single isolated environment.
![GNS3](https://img.shields.io/badge/GNS3-2.2.x-blue)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED)
![Python](https://img.shields.io/badge/Python-Automation-3776AB)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939)
![Modbus](https://img.shields.io/badge/Protocol-Modbus%2FTCP-orange)
![ICS%2FOT](https://img.shields.io/badge/Focus-ICS%2FOT%20Security-red)

---

## Overview

This project is a fully virtualized freshwater treatment **ICS/OT cyber range** designed to reproduce the architecture, networking, monitoring, and cybersecurity challenges found in industrial environments.

The environment models a simplified water-treatment facility consisting of:

**Raw Water Intake → Filtration → Chemical Dosing → Finished Water Storage**

Each process stage contains simulated industrial sensors and a dedicated PLC connected through segmented field networks. A centralized operations network provides SCADA, HMI, historian, and security-testing access.

The complete environment is designed to be **reproducible and automatically deployed** using Python, Docker, Jenkins, and the GNS3 API.

The cyber range is intended for authorized educational use and provides a controlled environment for studying industrial protocols, network segmentation, asset discovery, process monitoring, attack impact, anomaly detection, and OT incident response.

---

# Architecture

```text
                         FRESHWATER TREATMENT PROCESS
                         
      ┌──────────────┐
      │  Raw Water   │
      │    Intake    │
      └──────┬───────┘
             │
             ▼
      ┌──────────────┐
      │  Filtration  │
      └──────┬───────┘
             │
             ▼
      ┌──────────────┐
      │   Chemical   │
      │    Dosing    │
      └──────┬───────┘
             │
             ▼
      ┌──────────────┐
      │   Finished   │
      │ Water Storage│
      └──────┬───────┘
             │
             ▼
         Distribution

### Operations Network

The operations network connects the supervisory and control systems used to monitor the treatment process.

| System | Address |
|---|---|
| SCADA | `10.10.20.200` |
| HMI | `10.10.20.20` |
| Historian | `10.10.20.30` |
| Kali Linux | `10.10.20.250` |
| Intake PLC | `10.10.20.11` |
| Filtration PLC | `10.10.20.12` |
| Dosing PLC | `10.10.20.13` |
| Storage PLC | `10.10.20.14` |

### Field Networks

Each process area has its own field subnet containing sensors and the field-facing interface of its PLC.

| Process Area | Field Network | PLC Field Address |
|---|---|---|
| Intake | `192.168.10.0/24` | `192.168.10.5` |
| Filtration | `192.168.20.0/24` | `192.168.20.5` |
| Dosing | `192.168.30.0/24` | `192.168.30.5` |
| Storage | `192.168.40.0/24` | `192.168.40.5` |

This separation models the relationship between field instrumentation, PLC control, and supervisory systems found in industrial environments.

---

## Technologies

- **GNS3** — network and ICS topology simulation
- **Docker** — reusable industrial service containers
- **Python** — topology automation and deployment logic
- **Jenkins** — automated CI/CD deployment
- **SCADA** — operator interface and process visualization
- **PLCs** — industrial control logic and Modbus/TCP endpoints
- **Modbus/TCP** — simulated industrial communications
- **Kali Linux** — authorized security assessment workstation

---

## Deployment Model

The environment is designed to be reproducible instead of manually assembled for each deployment.

The general workflow is:

```text
GitHub
   │
   ▼
Jenkins
   │
   ├── Build deployment image
   ├── Build SCADA image
   └── Push container image
   │
   ▼
GNS3 API
   │
   ├── Create project
   ├── Create nodes
   ├── Configure networks
   ├── Create links
   └── Start topology
   │
   ▼
Running Freshwater Treatment Cyber Range
