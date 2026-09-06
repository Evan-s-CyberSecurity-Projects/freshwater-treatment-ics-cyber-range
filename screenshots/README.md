# Screenshots

This directory contains visual evidence from the freshwater treatment ICS cyber range. The screenshots demonstrate the deployed GNS3 topology, automated deployment pipeline, SCADA process visualization, OT network discovery, and live process telemetry.

## Evidence Overview

### GNS3 Topology

**File:** `gns3-topology.png`

The GNS3 topology shows the complete freshwater treatment environment, including:

- Four process areas
- Field sensors
- Four PLCs
- Field network switches
- Operations network
- HMI
- Historian
- SCADA server
- Kali Linux security workstation

This screenshot demonstrates the physical and logical structure of the simulated industrial control system.

### SCADA P&ID

**File:** `scada-pid.png`

The SCADA interface provides a process-level view of the freshwater treatment system. It represents the major treatment stages and displays live process values associated with the simulated sensors and PLCs.

This demonstrates how operational technology telemetry can be presented to operators through an HMI/SCADA interface.

### Jenkins Deployment

**File:** `jenkins-deployment.png`

The Jenkins console demonstrates automated deployment of the freshwater treatment cyber range.

The pipeline builds the required container images, prepares the deployment environment, creates the GNS3 topology, starts the required nodes, and completes the deployment successfully.

This demonstrates reproducible CI/CD-based infrastructure deployment rather than relying on manual topology creation.

### Kali Modbus/TCP Scan

**File:** `kali-modbus-scan.png`

The Kali Linux security workstation performs an authorized discovery scan against the four PLC endpoints.

The scan demonstrates:

- Four PLC hosts responding
- TCP/502 exposed on the PLCs
- Modbus/MBAP traffic being detected
- Successful OT network service discovery

This provides evidence of the simulated industrial protocol attack surface within the isolated cyber range.

### Live Sensor Trends

**File:** `sensor-trends.png`

The SCADA Trends interface displays changing process telemetry from the simulated freshwater treatment environment.

The changing values demonstrate that the system is not simply displaying static data; the sensor models are producing continuously changing process conditions that can be observed through the SCADA system.

## Portfolio Context

Together, these screenshots demonstrate the full operating workflow of the cyber range:

**Build → Deploy → Operate → Observe → Assess**

The environment is designed as an isolated and authorized platform for learning and demonstrating industrial control system (ICS) and operational technology (OT) cybersecurity concepts.
