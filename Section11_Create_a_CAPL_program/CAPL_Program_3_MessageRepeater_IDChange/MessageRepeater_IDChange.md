
# CAPL Program: CAN Message Repeater with ID Change

---

## Problem Statement
Listen for incoming CAN messages with ID **0x100**, create a copy of the received message, change its ID to **0x200**, and retransmit it onto the bus.

Purpose: Demonstrate basic CAPL operations like message capture, modification, and retransmission.

---

## How it Works
- A **blank message** (`modifiedMsg`) with ID **0x200** is created.
- When a message with ID **0x100** is received:
  - All **8 data bytes** and **DLC** from the original message are copied manually.
  - The ID is changed to **0x200** by using the blank message.
  - The modified message is **transmitted**.

---

## Restrictions (View-Only Mode Limitation)
- In **Vector CANoe View-Only mode**, live message transmission (`output()`) **may not reflect** on the actual CAN bus.
- Code compilation and logic simulation succeed, but bus interaction might not be observed.


---

## Expected Output 
| Step                        | Action                                            |
|------------------------------|---------------------------------------------------|
| 1. Incoming message detected | A message with ID 0x100 is received.              |
| 2. Cloning + ID modification | Data copied; ID changed to 0x200 internally.      |
| 3. Re-transmission attempt   | Modified message is sent back on the CAN bus.     |
| 4. Write Window (Log)        | Heartbeat and cloned-message info optionally printed. (if added) |

---

## Real-World Application Examples
- **Gateway ECU Simulation**: Replicating and forwarding messages between two CAN networks with modified IDs.
- **Test Automation**: Creating test scenarios where **fault injection** or **ID remapping** is required without affecting original traffic.
- **Security Testing**: Simulating message spoofing attacks by cloning valid frames with different IDs.
- **Load Testing**: Repeating valid messages with modified IDs to check system robustness.

---

## Files Included
| File Name | Description |
|-----------|-------------|
| `CAN_Message_Repeater_ID_Change.can` | CAPL source code (capture, modify, transmit logic) |
| `message_repeater_code_success.png` | Compilation success screenshot |
| `message_repeater_demo_VIEWONLY_LIMITATION.png` | Runtime demo screenshot showing View-Only restrictions |

---

## Important Concepts Practiced
- CAPL `on message` event handling
- Manual byte-by-byte data copying
- Message ID manipulation
- CAN output transmission

---

This CAPL program was developed under **CANoe View-Only Mode**.  
In licensed environments, this script would **actively capture, modify, and resend frames** on the CAN bus.

