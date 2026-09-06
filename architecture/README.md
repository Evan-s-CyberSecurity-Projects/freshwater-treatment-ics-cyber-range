# System Architecture

This directory documents the architecture of the Freshwater Treatment
ICS Cyber Range.

The environment is designed as a small industrial control system (ICS)
representing a freshwater treatment facility while remaining fully isolated
and reproducible for cybersecurity training.

The architecture is divided into three primary layers:

1. Process / Field Layer
2. Operations / Control Layer
3. Security / Management Layer

---

## Architecture Overview

```text
                    FRESHWATER TREATMENT PROCESS

       Raw Water
          │
          ▼
    ┌──────────────┐
    │    Intake    │
    │     PLC      │
    └──────┬───────┘
           │
           ▼
    ┌──────────────┐
    │  Filtration  │
    │     PLC      │
    └──────┬───────┘
           │
           ▼
    ┌──────────────┐
    │   Chemical   │
    │    Dosing    │
    │     PLC      │
    └──────┬───────┘
           │
           ▼
    ┌──────────────┐
    │   Storage    │
    │     PLC      │
    └──────┬───────┘
           │
           ▼
      Finished Water
