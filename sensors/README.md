# Sensor Architecture

The Freshwater Treatment ICS Cyber Range uses sixteen simulated industrial
sensors to represent process instrumentation throughout the treatment plant.

The sensors provide continuous process telemetry to the corresponding PLCs,
which then expose aggregated process data to the operations network.

```text
Industrial Sensor
       │
       ▼
   Field Network
       │
       ▼
      PLC
       │
       │ Modbus/TCP
       ▼
Operations Network
       │
   ┌───┼───────────┐
   ▼   ▼           ▼
 SCADA HMI     Historian
