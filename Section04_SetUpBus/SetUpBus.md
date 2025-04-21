# Section 04 – Set Up the Bus

This section focused on defining the bus parameters and assigning simulation nodes to the network **CAN 1 (Comfort)**.

---

## What Was Done (View-Only Mode)

### 1. Network Topology & Bitrate Setup
- Accessed **Simulation Setup** and right-clicked `CAN 1` to open `Network Hardware Configuration`.
- **Bitrate was configured to 500 kbps**.
- Hardware Type/Controller remained **Unavailable** due to View-Only license.

`section4_can1_bitrate_config.png`

---

### 2. Bus Configuration Panel (CAN 1)
- Explored CAN Controller settings.
- Could not activate real CAN hardware interface.

`section4_can1_network_config_panel.png`

---

### 3. Assign Nodes to Bus (View Mode)
- Created mock simulation nodes under `Comfort > Nodes` like `Test 26`, `Test 27`, etc.
- These are *virtual representations* for network design only (non-functional in View-Only mode).

`section4_simulation_nodes_assigned_to_bus.png`

---

### 4. Assign Module (View-Only)
- Triggered the panel for module assignment using right-click → “Assign Module”.
- Opened `.vmod` file browser, but no module assignment could be completed.

`section4_assign_module_browse_panel.png`

---

### 5. Final Bus Layout (View)
- Aligned all ECUs and replay blocks visually to match simulation bus layout.
- Ready for visualization or documentation.

`section4_network_final_layout.png`

---

## What Could Be Done in Licensed Mode (Pro Version)

| Step | Licensed Mode Features |
|------|------------------------|
| CAN Controller Config | Assign real CAN hardware (e.g., Vector CANcaseXL). |
| Bitrate Setup | Scan and synchronize bitrate using actual hardware. |
| Assign Modules | Assign `.vmod` modules for CAPL or Signal Generation. |
| Node Execution | Run simulated nodes and observe signal exchange. |
| Trace Panels | Live data capture, error frame observation, CAN load metrics. |
| Logging | Enable `.blf` or `.asc` log file generation for real-time bus activity. |

---

## Summary

| Mode | What We Did |
|------|-------------|
| **View-Only** | Configured layout, bitrates, and visualized simulation topology. |
| **Licensed** | Would allow full interaction with real CAN networks, signal injection, and live bus diagnostics. |

This section helps in understanding how to map out CAN communication flow and is crucial before defining symbolic signals or CAPL logic in later stages.

