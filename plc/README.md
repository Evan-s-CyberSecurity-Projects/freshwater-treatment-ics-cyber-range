# PLC Architecture

This directory documents the programmable logic controllers (PLCs) used by
the Freshwater Treatment ICS Cyber Range.

The environment contains four process PLCs, with each PLC responsible for a
distinct stage of the freshwater treatment process.

```text
Raw Water Intake
       ↓
   Intake PLC
       ↓
Filtration
       ↓
Filtration PLC
       ↓
Chemical Dosing
       ↓
Dosing PLC
       ↓
Finished Water Storage
       ↓
Storage PLC
