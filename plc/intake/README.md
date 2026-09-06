
Then each process gets a small technical README.

### `plc/intake/README.md`

```markdown
# Intake PLC

## Role

The Intake PLC represents the control system responsible for the raw-water
intake stage.

## Network

Operations network:

`10.10.20.11/24`

Field network:

`192.168.10.5/24`

Field subnet:

`192.168.10.0/24`

## Sensors

- `FT-INTAKE` — Flow
- `LT-INTAKE` — Level
- `DP-INTAKE` — Differential Pressure
- `TU-INTAKE` — Turbidity

## Industrial Protocol

Modbus/TCP — TCP/502

## Security Relevance

The Intake PLC is a process-control asset whose compromise could affect
simulated raw-water intake telemetry and downstream process behavior.

## Related

- [PLC Architecture](../README.md)
- [Sensor Architecture](../../sensors/README.md)
- [Security](../../security/README.md)
