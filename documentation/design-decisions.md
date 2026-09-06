
---

## `documentation/design-decisions.md`

```markdown
# Design Decisions

This document records the major architectural and engineering decisions
behind the Freshwater Treatment ICS Cyber Range.

The goal is to explain not only what was built, but why it was built that
way.

---

# Why GNS3?

GNS3 provides a flexible environment for modeling networked infrastructure and
connecting multiple virtualized systems into a topology.

It allows the project to represent:

- Field networks
- Operations networks
- PLCs
- Sensors
- SCADA
- HMI
- Historian
- Security workstations

The topology can also be recreated programmatically through the GNS3 API.

---

# Why Docker?

Docker provides consistent, reusable environments for the simulated
industrial components.

Containerization makes it practical to reuse:

- PLC images
- Sensor images
- HMI images
- SCADA images

It also allows scenario-specific configuration to be layered onto reusable
base images.

---

# Why Python?

Python is used as the primary deployment automation language.

It provides access to:

- GNS3 APIs
- HTTP APIs
- Configuration logic
- Validation
- Error handling

Python also makes the deployment logic easier to maintain than a collection
of manual procedures.

---

# Why Jenkins?

Jenkins provides a repeatable CI/CD entry point.

The pipeline can:

```text
Build
  ↓
Publish
  ↓
Deploy
  ↓
Validate
