# Storage PLC

## Role

The Storage PLC represents the control system responsible for finished-water
storage.

## Network

Operations network:

`10.10.20.14/24`

Field network:

`192.168.40.5/24`

Field subnet:

`192.168.40.0/24`

## Sensors

- `LT-STORAGE` — Level
- `TU-STORAGE` — Turbidity
- `CL-STORAGE` — Chlorine
- `TT-STORAGE` — Temperature

## Industrial Protocol

Modbus/TCP — TCP/502

## Security Relevance

The Storage PLC provides telemetry for the finished-water stage and can be
used to study the relationship between process anomalies and OT security
events.

## Related

- [PLC Architecture](../README.md)
- [Sensor Architecture](../../sensors/README.md)
- [Security](../../security/README.md)
