
---

## `documentation/plc.md`

```markdown
# PLC Operations Guide

This document describes the four PLCs used by the Freshwater Treatment ICS
Cyber Range.

Each PLC represents a distinct treatment stage and is dual-homed between its
field network and the centralized operations network.

---

# PLC Overview

| PLC | Process | Field IP | Operations IP |
|---|---|---:|---:|
| Intake PLC | Raw Water Intake | `192.168.10.5` | `10.10.20.11` |
| Filtration PLC | Filtration | `192.168.20.5` | `10.10.20.12` |
| Dosing PLC | Chemical Dosing | `192.168.30.5` | `10.10.20.13` |
| Storage PLC | Finished Water Storage | `192.168.40.5` | `10.10.20.14` |

---

# PLC Communication

The PLCs use:

```text
Modbus/TCP
TCP/502
