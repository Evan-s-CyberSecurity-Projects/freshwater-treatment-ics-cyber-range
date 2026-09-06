# Filtration PLC

## Role

The Filtration PLC represents the control system responsible for the
filtration stage of the treatment process.

## Network

Operations network:

`10.10.20.12/24`

Field network:

`192.168.20.5/24`

Field subnet:

`192.168.20.0/24`

## Sensors

- `TU-FILTRATION` — Turbidity
- `DP-FILTRATION` — Differential Pressure
- `FT-FILTRATION` — Flow
- `LT-FILTRATION` — Level

## Industrial Protocol

Modbus/TCP — TCP/502

## Security Relevance

Filtration telemetry provides visibility into filter performance and process
conditions. Unexpected changes can indicate either process problems or
security-relevant manipulation.

## Related

- [PLC Architecture](../README.md)
- [Sensor Architecture](../../sensors/README.md)
- [Security](../../security/README.md)
