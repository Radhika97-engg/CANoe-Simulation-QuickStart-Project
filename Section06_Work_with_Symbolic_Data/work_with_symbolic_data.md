# Section 6: Work with Symbolic Data

## Objective:
Understand how to link a DBC file, interpret symbolic CAN data, and analyze message/signal parameters using CANdb++ Editor and the Trace window.

---

## Tasks Performed in View-Only Mode

### 6.1 Assign a Database
- Accessed **Simulation Setup → Databases → Add…**
- Assigned **PowerTrain.dbc** to the `Comfort` network.
- Verified DBC linking in system view.

Screenshots:
- `section6_add_database_dialog.png`
- `section6_dbc_assigned_network_view.png`

---

### 6.2 Display in the Trace Window (Simulation Blocked)
- Opened **Trace PowerTrain** window.
- Loaded DBC → symbolic headers (ID, Name, Data) visible.
- Could not populate messages due to view-only mode.

Screenshot:
- `section6_view_trace_window_powertrain.png`

---

### Explored CANdb++ Editor
- Opened **PowerTrain.dbc** in CANdb++ Editor.
- Located signal `EngTemp` (Temperature in degC).
- Understood encoding:  
  - `Length`: 7 bits  
  - `Factor`: 2  
  - `Offset`: -50  
  - Physical value = (RawValue × 2) - 50

Screenshots:
- `section6_powertrain_dbc_content.png`
- `section6_engtemp_signal_properties.png`

---

## View-Only Mode Limitations

| Feature                             | Status   |
|-------------------------------------|----------|
| Assign DBC                          | Allowed  |
| View Signal Definitions             | Allowed  |
| Open CANdb++ Editor                 | Allowed  |
| Run Measurement                     | Blocked  |
| View Message in Trace (Live Replay) | Blocked  |

---

## What I Could Do with a Full License:
- Start measurement and **observe symbolic messages** in real-time.
- Track **EngineData** and **EngTemp** in Trace/Graphics/Data windows.
- Validate payload conversions to physical units.
- Enable message-triggered actions (like logging, exporting, or alerts).

---

Folder: `Section06_Work_with_Symbolic_Data`  


---
