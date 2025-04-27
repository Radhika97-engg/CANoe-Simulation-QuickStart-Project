
# CAPL Program 5 – Vehicle Speed Monitor & Threshold Logger

---

## Program Description

This CAPL script monitors incoming CAN messages containing **Vehicle Speed** information (ID `0x400`).  
If the Vehicle Speed crosses a critical threshold of **120 km/h**, a warning is logged in the CANoe Write Window.  
This simulates real-world threshold monitoring used in automotive ECU validation.

---

## Implementation Details

- Listens for incoming CAN message **ID 0x400**.
- Reads **Byte 0** assuming it holds an unsigned 8-bit VehicleSpeed value.
- Checks if the **Vehicle Speed > 120 km/h**.
- Logs a **high-speed warning** message when the threshold is crossed.

on message 0x400
{
    vehicleSpeed = this.byte(0);
    if (vehicleSpeed > 120)
    {
        write("Vehicle Speed High Warning! Speed = %d km/h", vehicleSpeed);
    }
}
```

---

## Limitations (View-Only Mode)

- Due to **CANoe View-Only License**:
  - Simulation cannot be started to trigger real CAN message reception.
  - Write Window warning logs based on actual message reception are **not visible**.
- In a fully licensed CANoe environment:
  - Real CAN messages would be received and warnings would be displayed live.

---

## Expected Output (Licensed Environment)

- Every time a CAN message with ID **0x400** is received:
  - If the decoded speed > 120 km/h:
    - The following warning would appear in the Write Window:
    > Vehicle Speed High Warning! Speed = 135 km/h

---

## Real-World Application

- **Automotive Validation**:  
  Used in vehicle ECU testing to monitor critical signals like speed, RPM, temperature, and voltage against safe operating thresholds.

- **Safety System Testing**:  
  Verifying that systems react appropriately to abnormal or dangerous vehicle behavior (e.g., sending warnings to dashboard clusters or triggering failsafe mechanisms).

- **Case Example**:  
  In a real validation project for an Electric Vehicle (EV), VehicleSpeed monitoring scripts are deployed to ensure the car does not exceed safe speeds without properly activating alarms or driver notifications.

---

## Files Included

| File Name | Description |
| :-------- | :---------- |
| `CAPL_VehicleSpeed_Monitoring_Logger.can` | CAPL script for threshold-based speed monitoring |
| `vehicle_speed_monitor_demo_VIEWONLY.png` | Screenshot demonstrating compilation success and view-only limitation |

---
