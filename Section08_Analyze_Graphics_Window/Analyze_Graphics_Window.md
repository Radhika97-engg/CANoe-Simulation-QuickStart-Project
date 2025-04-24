# Section 08: Analyze Signal Responses in Graphics Window (View-Only Mode)

This section follows the CANoe Quick Start Guide and explores how to visualize CAN signal responses over time using the Graphics Window in View-Only Mode.

## Key Learnings

- Open and configure the Graphics Window.
- Select symbolic signals from a database (DBC).
- Display time-sequenced signal values using "Steps" connection type.
- Understand limitations of View-Only mode.

---

## Screenshots & What Was Done

### 1️`section8_open_graphics_window_menu.png`
- Opened Graphics Window via **Analysis > Graphics > New > Graphics Window**.

### 2️`section8_symbol_selection_gearboxinfo.png`
- Navigated to the **PowerTrain > Frames > GearBoxInfo** message to select signals (Gear, EcoMode, ShiftRequest).

### 3️`section8_selected_signals_in_graphics_window.png`
- Signals were successfully added and shown in separate Y-axes by default.
- Could **view signal transitions over 10s**, including `Gear_5` steps and binary `ShiftRequest`.

### 4️`section8_graph_display_connection_type_step.png`
- Modified `Connection Type` to **Steps** for clearer visualization of discrete signal states.

---

## View-Only Mode Limitations

- Cannot simulate dynamic transitions or animate the bus in real-time.
- Cannot **overlay all graphs in one shared Y-axis** — `Create Common Axis/Group` is **disabled**.
- Export and logging features (e.g. `.mat` or `.csv` format) are not available.

---

## In Licensed Mode

- Run full simulations and dynamically populate graphs.
- Combine signals on common axes for correlation.
- Export graph data and synchronize measurements with other panels.

---

## Folder Structure
Section08_Analyze_Signal_Responses
├── section8_open_graphics_window_menu.png
├── section8_symbol_selection_gearboxinfo.png 
├── section8_selected_signals_in_graphics_window.png 
├── section8_graph_display_connection_type_step.png 
└── README.md


---
Next: [Log a Measurement →](../Section09_Log_Measurement)

