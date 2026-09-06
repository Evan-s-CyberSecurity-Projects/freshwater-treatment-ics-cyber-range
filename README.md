# Freshwater Treatment ICS Cyber Range

> A reproducible industrial control system (ICS) and operational technology (OT) cyber range modeling a freshwater treatment facility for cybersecurity training, attack simulation, monitoring, and incident-response exercises.

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
