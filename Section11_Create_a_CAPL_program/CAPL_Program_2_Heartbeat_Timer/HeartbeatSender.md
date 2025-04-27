
# CAPL Program 2 – Heartbeat Timer

This CAPL script demonstrates how to use timers in CANoe to periodically simulate a "heartbeat" message, mimicking how ECUs send periodic signals to indicate their availability on the network.

---

## Objective

To simulate sending a heartbeat message every 1 second using CAPL's `msTimer` and `setTimer()` functionality.

---

## Logic Overview

- A `msTimer` named `heartbeatTimer` is initialized.
- The timer is started in the `on start` event with a 1000ms delay.
- In the `on timer heartbeatTimer` event:
  - A simulated "heartbeat sent" message is printed using `write()`.
  - The timer is restarted to repeat the process indefinitely.

---

## Files Included

| File | Description |
|------|-------------|
| `HeartbeatSender.can` | CAPL source code |
| `heartbeat_sender_code_success.png` | Screenshot of successful compilation |
| `heartbeat_sender_demo_VIEWONLY_LIMITATION.png` | Write Window output showing View-Only Mode limitations |
| `README.md` | This documentation file |

---

## Output (Expected in Licensed Version)

```
Heartbeat msg sent at: 1000 ms
Heartbeat msg sent at: 2000 ms
Heartbeat msg sent at: 3000 ms
...
```

These would appear in the **Write Window** every 1000 ms.

---

## CANoe View-Only Limitation

As seen in the included screenshot `heartbeat_sender_demo_VIEWONLY_LIMITATION.png`, the **Write Window output is blocked** due to the restricted license:

 `CANoe /pro version limitations: Starting of measurement (online/offline)`  
  Therefore, `write()` statements and real-time simulation behaviors are not visible.

However, the script **compiles successfully** and is expected to run correctly in a fully licensed CANoe setup.

---

## Real-World Application

Heartbeat messages are essential in safety-critical automotive systems. For example:

- **Body Control Module (BCM)** periodically sends its presence.
- **Battery Management System (BMS)** emits a regular heartbeat to signal it is online.
- If a heartbeat is missed for a certain duration, **fault diagnostics** can be triggered.

This timer-based simulation is a stepping stone to validating watchdogs and timeout monitoring in larger embedded validation frameworks.

---

Created as part of the **CANoe Simulation QuickStart Learning Project**