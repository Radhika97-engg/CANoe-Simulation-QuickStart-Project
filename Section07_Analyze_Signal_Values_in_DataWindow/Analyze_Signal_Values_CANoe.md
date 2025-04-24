## Section 7: Analyze Signal Values in Data Window

### Objective
Use the **Data Window** in CANoe to monitor and analyze decoded signal values from a symbolic CAN message (EngineData, ID 0x40).

---

### Step-by-Step Summary

#### 7.1 Add Signals in the Data Window  
**View-Only Mode – What I Did:**
- Opened the **Data Window** via `Analysis → Data`.
- Used `Right-click → Add Signals…` to launch the Symbol Selection dialog.
- Selected multiple signals from the PowerTrain DBC file.

Screenshots:
- `section7_data_window_opened.png`
- `section7_symbol_selection_powertrain_signals.png`

Licensed Mode – What I Could Have Done:
- Seen real-time **signal values**, **raw values**, and **bar graphs** dynamically updating during simulation.

---

#### 7.1.2 Display in the Data Window  
**View-Only Mode – What I Did:**
- Confirmed symbolic names (like `EngSpeed`, `EngTemp`, `IdleRunning`) were visible in the Data Window with their respective units.
- Observed placeholders (`--`) under **Value**, **Raw Value**, and **Bar**, indicating that simulation was not running.

Screenshot:
- `section7_data_window_with_signal_values.png`

Licensed Mode – What I Could Have Done:
- Viewed live decoding of CAN signals in human-readable format.
- Visualized signal status (e.g., engine running, gear position) through dynamic bars and value fields.

---

### View-Only Mode Summary

| Feature                             | Status     |
|-------------------------------------|------------|
| Open Data Window                    | Allowed    |
| Browse & Add DBC Signals            | Allowed    |
| View Live Signal Data               | Blocked    |
| Bar Graph Visualizations            | Blocked    |

---

### What This Demonstrates to Recruiters
Even without a licensed version:
- I showcased familiarity with adding symbolic signals from a DBC.
- Followed standard procedures used in validation workflows.
- Emulated real-world setup engineers use to trace CAN messages and diagnostics.

---