
## `security/incident-scenarios/unauthorized-write.md`

```markdown
# Incident Scenario: Unauthorized Write Investigation

## Objective

Investigate a controlled industrial data-change event and determine whether
the change was authorized.

This scenario is designed for the isolated Freshwater Treatment ICS Cyber
Range.

---

## Scenario

An unexpected change is observed in process telemetry.

The analyst must determine whether the change was caused by:

- Legitimate operator activity
- Expected simulation behavior
- Process disturbance
- Unauthorized control activity

---

## Learning Objectives

The analyst should learn how to:

- Identify unexpected process changes
- Correlate process telemetry with network activity
- Identify the source of industrial activity
- Review SCADA/HMI context
- Determine likely cause
- Document evidence

---

## Investigation Flow

```text
Unexpected Process Change
          ↓
Review Sensor Data
          ↓
Review PLC Activity
          ↓
Review Modbus Activity
          ↓
Review SCADA / HMI Activity
          ↓
Identify Source
          ↓
Determine Authorization
          ↓
Document Finding
