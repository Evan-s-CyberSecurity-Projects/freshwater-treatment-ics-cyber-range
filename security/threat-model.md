
## `security/threat-model.md`

```markdown
# Threat Model

This document describes the primary security threats considered by the
Freshwater Treatment ICS Cyber Range.

The purpose is not to model every possible real-world attack, but to identify
the highest-value assets, trust boundaries, attack paths, and operational
consequences represented by the laboratory.

---

# Assets

| Asset | Primary Security Concern | Potential Consequence |
|---|---|---|
| SCADA | Unauthorized access or configuration changes | Loss of monitoring/control |
| PLCs | Unauthorized commands or configuration | Process manipulation |
| HMI | Unauthorized operator actions | Incorrect control decisions |
| Historian | Data manipulation or loss | Reduced investigation capability |
| Sensors | False or missing telemetry | Incorrect process state |
| Modbus/TCP | Unauthorized access | Industrial communication abuse |
| Jenkins | Pipeline compromise | Unauthorized deployment |
| Docker images | Malicious or altered image | Compromised deployed services |
| GitHub | Source/workflow compromise | Supply-chain risk |
| GNS3 API | Unauthorized management access | Topology/environment compromise |

---

# Trust Boundaries

The environment contains several important trust boundaries.

```text
IT / CI-CD
    │
    │
    ▼
Deployment Layer
    │
    │
    ▼
OT Operations
    │
    │
    ▼
PLC Operations
    │
    │
    ▼
Field Networks
    │
    │
    ▼
Process
