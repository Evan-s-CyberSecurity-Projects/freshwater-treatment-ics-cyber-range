
---

## `documentation/network.md`

```markdown
# Network Architecture

This document describes the network design and addressing used by the
Freshwater Treatment ICS Cyber Range.

The network is divided into an operations network and four process-specific
field networks.

---

## Network Overview

```text
                       OPERATIONS NETWORK
                         10.10.20.0/24

        ┌─────────┬──────────┬──────────┬──────────┐
        │         │          │          │          │
       SCADA     HMI      Historian    Kali       PLCs
       .200      .20        .30       .250      .11-.14
                                             
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
       Intake        Filtration       Dosing       Storage
       Field Net     Field Net        Field Net    Field Net
       .10.0/24      .20.0/24         .30.0/24     .40.0/24
