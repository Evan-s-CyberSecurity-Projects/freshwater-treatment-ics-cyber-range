# SCADA

This directory contains the freshwater-specific SCADA configuration and
process visualization for the Freshwater Treatment ICS Cyber Range.

The project extends a reusable containerized SCADA platform with a custom
freshwater-treatment scenario and industrial process visualization.

---

## SCADA Architecture

```text
                    FRESHWATER TREATMENT SCADA

                         ┌───────────────┐
                         │     SCADA     │
                         │ 10.10.20.200  │
                         └───────┬───────┘
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
              ▼                  ▼                  ▼
         Intake PLC        Filtration PLC      Dosing PLC
         10.10.20.11       10.10.20.12         10.10.20.13
              │                  │                  │
              └──────────────────┼──────────────────┘
                                 │
                                 ▼
                            Storage PLC
                           10.10.20.14
