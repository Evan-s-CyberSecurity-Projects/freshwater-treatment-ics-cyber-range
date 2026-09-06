# Dosing PLC

## Role

The Dosing PLC represents the control system responsible for chemical dosing
within the treatment process.

## Network

Operations network:

`10.10.20.13/24`

Field network:

`192.168.30.5/24`

Field subnet:

`192.168.30.0/24`

## Sensors

- `CL-DOSING` — Chlorine
- `PH-DOSING` — pH
- `FT-DOSING` — Process Flow
- `FT-DOSE` — Chemical Dose Flow

## Industrial Protocol

Modbus/TCP — TCP/502

## Security Relevance

Chemical dosing is a high-consequence process area because changes to
chemical-related telemetry or control behavior can affect simulated water
quality.

## Related

- [PLC Architecture](../README.md)
- [Sensor Architecture](../../sensors/README.md)
- [Security](../../security/README.md)
