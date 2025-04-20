# Section 1: Overview of CANoe

## What is CANoe?

**CANoe** is a comprehensive development, simulation, and test tool from Vector Informatik. It is widely used in the automotive and embedded industries to validate the communication behavior of ECUs (Electronic Control Units) across various network protocols such as:

- **CAN** (Controller Area Network)
- **LIN** (Local Interconnect Network)
- **FlexRay**
- **Ethernet**
- **MOST**

---

## Where CANoe Fits in the Industry

CANoe supports engineers throughout the product development lifecycle:

| Stage | How CANoe is Used |
|-------|--------------------|
| **Development** | Simulate ECUs, create virtual nodes |
| **Testing** | Monitor and validate real bus traffic |
| **Validation** | Check compliance with DBC/database, timing, behavior |
| **Integration** | Ensure inter-ECU communication works as intended |
| **Vehicle Testing** | Log data from test drives, replay logs for debugging |

---

## Modes of Operation

- **Full Mode:** Allows node simulation, CAPL execution, logging, real-time analysis
- **View-Only Mode (used in this project):**
  - Explore interface
  - Load logs
  - View configuration
  - Load DBCs and trace signals
  - **Write but not run CAPL scripts**

---

## Objective of This Project

To self-learn CANoe using **Vector’s official Quick Start Guide** and recreate the learning process in View-Only Mode, including:

- Configuration structure
- Signal decoding from DBC
- Simulation block layout
- Trace analysis
- Basic CAPL scripting

---

## Reference

- Vector Quick Start Guide – *CANoe QuickStartExp.pdf*
- Vector CANoe Help Documentation

---
**Next Step →** [Section 2: Creating a New Configuration](02_NewConfig.md)
