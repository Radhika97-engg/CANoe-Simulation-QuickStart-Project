
# Section 5: Transmit Data Without Database

## Objective  
Manually transmit CAN messages using a **visual sequence** without a CAN database and observe system behavior.

---

## Task 1: Send a Basic CAN Message (ID: 0x40)

### Configuration Details:
- **Identifier**: `0x40`  
- **Payload**: `D8 D6 37 00`  
- **Cycle time**: `100 ms`  

### Steps Performed in View-Only Mode:
1. Opened **Automation Sequences** from `Simulation` tab  
   `section5_message_1_empty.png`
2. Created a new sequence: **Message 1**
3. Added command:
   - `Send CAN Raw Frame`
   - **Channel**: CAN1  
   - **Identifier**: 0x40  
   `section5_send_can_message_visual_sequence.png`
4. Entered data bytes as operand: `D8 D6 37 00`
5. Set Wait time: `100 ms`
6. Tried to manually run the sequence  
    Got blocked with message:  
   `"Sequence can only be started while measurement is running"`  
   `section5_cannot_run_sequence.png`

---

## Task 2: Send Second Message Cyclically (ID: 0x3FC)

### Configuration Details:
- **Identifier**: `0x3FC`  
- **Payloads**: 01 → 05 (changing first byte each time)  
- **Cycle time**: `500 ms`

### Steps Performed:
1. Created **Message 2** sequence  
2. Added multiple rows with `Send CAN Raw Frame`, ID: 0x3FC  
3. Set operand values from `01` to `05`, one in each row  
4. Applied `500 ms` wait between each  
   `section5_message2_final_config.png`

---

## Trace Panel Exploration
- Opened **Trace Comfort** window via `Analysis > Trace`  
  `section5_trace_disabled.png.png`
- Confirmed no live trace due to **View-Only restriction**

---

## View-Only Mode Summary

| Feature                                 | Status    | Notes |
|-----------------------------------------|-----------|-------|
| Visual Sequence Panel Access            | Allowed  | Message 1 & 2 created |
| CAN Frame Configuration                 | Allowed  | All required fields filled |
| Payload Setup                           | Allowed  | Hex operands added |
| Simulation Start (Measurement)          | Blocked | Needed for runtime replay |
| Sequence Execution                      | Blocked | Cannot test flow |
| Trace Window (Live CAN Logging)         | Blocked | No runtime bus activity |
| Export Logs (CSV, MAT)                  | Blocked | Requires active simulation |

---

## What I Would Do with a Full License:
- Run simulation to test both messages
- Observe both CAN messages on **Trace** with real-time timestamps
- Verify periodicity and content
- Export logs to `.csv` or `.mat` for validation/reporting
- Activate auto-replay  to simulate message stream

---
## Real-World Application
In real automotive systems, engineers often manually inject or simulate CAN frames to:
**Test Module Responses**: Send specific IDs (e.g., Engine RPM, ABS faults) to verify if ECUs react properly.
**Validate Safety Systems**: Simulate sudden data patterns like vehicle overspeed, ABS triggers, or emergency brake signals.
**Diagnose Field Issues**: Replicate real-world faults by sending crafted CAN frames during workshops or recalls.
**Pre-validate ECU Communication**: Before full integration, teams transmit messages manually to ensure that all network nodes accept, reject, or acknowledge them correctly.

The skills practiced here — manual CAN frame configuration, cycle time tuning, and trace analysis — are fundamental in:
Vehicle Network Validation
Hardware-in-the-Loop (HIL) Testing
End-of-Line (EOL) Diagnostics in automotive manufacturing.

---
## Folder Contents

| Screenshot | Purpose |
|------------|---------|
| `section5_message_1_empty.png` | Created Message 1 sequence |
| `section5_send_can_message_visual_sequence.png` | Configured message 0x40 |
| `section5_cannot_run_sequence.png` | View-only error when trying to run |
| `section5_message2_final_config.png` | Configured Message 2 with ID 0x3FC |
| `section5_trace_disabled.png.png` | Trace Window shows no runtime data |
