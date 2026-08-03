# 🚀 PLC Knight Rider Light Sequencer (S7-300)

## 📌 Overview

This project implements a **Knight Rider (Lauflicht) LED sequencing system** using a Siemens S7-300 PLC (CPU 314C-2 DP) programmed in TIA Portal.

The system generates a moving light effect (left ↔ right) using structured PLC programming with Function Blocks (FB), Data Blocks (DB), and cyclic OB execution.

---

## ⚙️ Features

-  Bidirectional LED running light (Knight Rider effect)
-  Structured programming using FB15
-  Cyclic execution via OB1
-  Word-based shift register logic (`wAusgänge`)
-  Emergency Stop (EMO) safety integration
-  Reset functionality for initial state
-  Direction control (left/right shifting)

---

## 🧱 PLC Program Structure

### 🔹 OB1 – Main Cycle
- Executes the main program continuously
- Calls FB15 (Light Sequencer logic)

### 🔹 FB15 – Light Sequencer
- Implements shift register logic
- Controls LED movement direction
- Handles start/stop and reset conditions

### 🔹 DB13 – Light Control Data Block
Stores system states and control variables:

| Variable         | Type  | Description |
|----------------|------|-------------|
| xStart         | BOOL | Start sequence |
| xReset         | BOOL | Reset system |
| xRotateRechts  | BOOL | Direction control (right shift) |
| wAusgänge      | WORD | LED output pattern |
| xEMO           | BOOL | Emergency stop |

---

## 💡 Function Description

The system works by shifting a single active bit inside a **16-bit word (`wAusgänge`)**:

- If `xRotateRechts = TRUE` → shift right
- Else → shift left

Each bit represents one LED output.

This creates the characteristic **Knight Rider scanning light effect**.

---

## 🔌 Hardware Setup

- Siemens S7-300 CPU 314C-2 DP
- Digital Output Module (LED simulation or real outputs)
---

## 📊 Signal Overview

### Inputs
- Start button
- Reset button
- EMO (Emergency Stop)
- Direction control switch

### Outputs
- LED 1 → LED 6 (or mapped outputs)
- Word-based output via `wAusgänge`

---

## 🧠 Logic Summary

1. System starts via `xStart`
2. A single bit is initialized in `wAusgänge`
3. On each cycle:
   - Bit shifts left and right
   - Direction depends on `xRotateRechts`
4. EMO overrides all logic
5. Reset returns to initial position


---
## Autor

<div align="center">

### **Wessam Abo Zayed**

**Automatisierungstechnik | SPS-/PLC-Programmierung | Data Analyst**
</div>

## Kontakt

| Kontakt      | Link                                                                            |
| ------------ | ------------------------------------------------------------------------------- |
| **E-Mail**   | [abozayed.wessam@gmail.com](mailto:abozayed.wessam@gmail.com)                   |
| **LinkedIn** | [linkedin.com/in/wessam-abozayed](https://www.linkedin.com/in/wessam-abozayed/) |
| **GitHub**   | [github.com/wessam-abo-zayed](https://www.github.com/wessam-abo-zayed)                   |
| **Tableau Public** | [public.tableau.com/app/profile/wessam3726](https://public.tableau.com/app/profile/wessam3726) |
