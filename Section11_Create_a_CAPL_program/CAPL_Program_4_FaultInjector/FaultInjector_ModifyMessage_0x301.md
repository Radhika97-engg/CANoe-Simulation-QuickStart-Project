
# CAPL Program 4 – Fault Injector by Message Modification (Flip Byte 0)

---

## Program Description

This CAPL script simulates a **fault injection** mechanism by flipping all bits of the first byte (`byte 0`) of an incoming CAN message with ID `0x301`.  
Instead of modifying the original message directly, it creates a **new faulty message** (with the same ID) and transmits it onto the bus.

---

## Implementation Details

- Listens for incoming CAN message with ID **0x301**.
- On receiving the message:
  - Flips (`XOR with 0xFF`) all bits of **Byte 0**.
  - Copies the remaining message bytes (`Byte 1–7`) and DLC from the original message.
  - Sends the **new faulty message** (`faultyMsg`) onto the CAN bus.

---

## Limitations (View-Only Mode)

- Due to **CANoe View-Only Mode**:
  - Actual message transmission and fault injection **cannot be fully validated** on a live CAN bus.
  - **Write Window output** will only show compilation success, but **no real message effect** can be observed.
- In a fully licensed CANoe environment, the faulty message would be observable in **Trace Window**.

---

## Expected Output

- On every reception of message **0x301**, a **faulty version** is transmitted where:
  - Byte 0 is flipped.
  - All other bytes remain identical.
  - DLC (Data Length Code) is preserved.

---

## Real-World Application

- **Fault Injection Testing**:  
  Used by automotive validation engineers to simulate corrupted CAN signals and test how ECUs respond to unexpected data patterns.

- **Robustness Validation**:  
  Helps in verifying if critical systems like airbags, braking modules, or battery management units behave safely even under faulty communication conditions.

- **Case Example**:  
  A Battery Management System (BMS) ECU receives a message indicating the voltage level.  
  If the fault-injected message flips the byte representing voltage, the system should detect the corruption via CRC or timeout strategies.

---

## Files Included

| File Name | Description |
| :-------- | :---------- |
| `FaultInjector_Message0x300.can` | CAPL script to flip and retransmit modified message |
| `faultinjector_code_success.png` | Screenshot showing successful code compilation |
| `faultinjector_demo_VIEWONLY_LIMITATION.png` | Screenshot demonstrating view-only simulation limitation |

---

