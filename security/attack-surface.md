
## `security/attack-surface.md`

```markdown
# Attack Surface

This document describes the major attack surfaces represented by the
Freshwater Treatment ICS Cyber Range.

The attack surface is intentionally broad enough to demonstrate the
relationship between IT infrastructure, OT systems, industrial protocols,
and the physical process.

---

# Attack Surface Overview

```text
                       ATTACK SURFACE

        ┌─────────────────────────────────┐
        │          IT / CI-CD              │
        │                                  │
        │ GitHub                           │
        │ Jenkins                          │
        │ Docker                           │
        └────────────────┬────────────────┘
                         │
                         ▼
        ┌─────────────────────────────────┐
        │        OT OPERATIONS             │
        │                                  │
        │ SCADA                            │
        │ HMI                              │
        │ Historian                        │
        │ PLC Operations Interfaces        │
        └────────────────┬────────────────┘
                         │
                         ▼
        ┌─────────────────────────────────┐
        │      INDUSTRIAL PROTOCOLS       │
        │                                  │
        │ Modbus/TCP                      │
        │ TCP/502                         │
        └────────────────┬────────────────┘
                         │
                         ▼
        ┌─────────────────────────────────┐
        │         FIELD NETWORKS          │
        │                                  │
        │ Sensors                          │
        │ PLC Field Interfaces             │
        │ Field Switches                   │
        └────────────────┬────────────────┘
                         │
                         ▼
                    PROCESS
