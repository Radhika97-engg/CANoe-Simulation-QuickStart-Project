# Section 2: Create a New Configuration

## Objective

To explore how a CANoe configuration is opened and structured using the View-Only Mode, based on the official Vector Quick Start Guide.

---

## Steps Followed

1. Opened CANoe in View-Only Mode
2. Navigated to: Sample Configurations > CAN > System Configuration (CAN)
3. Loaded the `CANSystemDemo.cfg` file
4. This opened a prebuilt simulation environment including:
- Network nodes (ECUs)
- CAN bus
- Graphics and Trace panels

---

## Configuration Structure Overview

| Component | Description |
|-----------|-------------|
| **Simulation Setup Tree** | Hierarchical list of nodes, buses, databases, and panels |
| **PowerTrain and Comfort Networks** | Contains nodes like `Engine`, `Gateway`, `Dashboard` |
| **Panels** | Graphics, Control, Trace panels used for data display |
| **Logging Blocks** | ReplayBlocks simulate bus activity (View-Only access) |

---

## Screenshots

| Filename | Description |
|----------|-------------|
| `new_config_loaded.png` | Loaded config layout with panels visible |
| `simulation_tree_config.png` | Full Simulation Setup tree on the left |
| `panel_menu_expanded.png` | Analysis tab showing panel options: Graphics, Trace, Data |

All screenshots are saved in:  
`/Section02_NewConfiguration/screenshots/`

---

## Reflections

Even though I couldn’t create a new configuration in View-Only Mode, I was able to:
- Load and explore a realistic sample simulation setup
- Understand node connectivity, panel usage, and message replay blocks
- Learn how testing panels and signal trees are structured in industry-ready setups

---

**Next Step →** [Section 3: Interface Windows](../Section03_InterfaceWindows/03_Interface_Windows.md)

