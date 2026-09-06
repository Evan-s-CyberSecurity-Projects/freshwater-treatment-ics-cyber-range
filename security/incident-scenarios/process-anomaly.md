
## `security/incident-scenarios/process-anomaly.md`

```markdown
# Incident Scenario: Process Anomaly

## Objective

Determine whether an abnormal treatment-process measurement is the result
of normal variation, a process disturbance, equipment behavior, or a
cybersecurity event.

---

## Scenario

An operator observes an unexpected change in one or more process values.

Example telemetry categories include:

- Flow
- Level
- Differential pressure
- Turbidity
- Chlorine
- pH
- Temperature

---

## Learning Objectives

The analyst should be able to:

- Compare telemetry against a normal baseline
- Identify related sensor changes
- Examine PLC activity
- Examine network activity
- Correlate events
- Determine the most likely cause

---

## Investigation Flow

```text
Process Anomaly
      ↓
Establish Time of Change
      ↓
Compare With Baseline
      ↓
Check Related Sensors
      ↓
Check PLC Activity
      ↓
Check Network Activity
      ↓
Check SCADA / HMI
      ↓
Determine Likely Cause
