
---

# `sensors/simulation-profiles.md`

```markdown
# Sensor Simulation Profiles

This document describes how simulated sensor telemetry behaves during normal
operation.

The goal is to provide realistic changing values rather than static
measurements so that students can establish baselines and identify unusual
behavior.

---

## Simulation Model

The cyber range uses multiple simulation behaviors.

### Random Walk

A random-walk sensor changes gradually around a starting value while staying
within defined minimum and maximum limits.

Conceptually:

```text
Current Value
     ↓
Small Change
     ↓
New Value
     ↓
Repeat
