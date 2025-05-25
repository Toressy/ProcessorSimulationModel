# 🧠 ProcessorSim-Cpp

This project simulates a basic processor architecture in C++, demonstrating how registers, bitwise operations, and instruction interpretation work at a low level.

## 🔧 Project Description

The processor simulation includes:

- Emulation of 20-bit registers (R1, R2)
- Commands: `mov`, `move`, with left/right shift operations
- Bit-level shifting logic to simulate instruction execution
- Instruction decoding and status register (PS) management
- Program counter (PC) and Tact counter (TC) tracking

## 📂 Files Overview

| File                | Purpose                                           |
|---------------------|---------------------------------------------------|
| `lab2.TXT`          | Input file with simulated assembly instructions   |
| `main.cpp` (inlined in report) | Main simulation program               |
| `Звіт Титаренко.docx` | Lab report describing the implementation       |
| `README.md`         | This documentation file                          |

## 🧪 Instruction Format Example

`lab2.TXT` contains commands like:

    mov R1,-78
    mov R2,298
    move R1,left
    move R2,right


Each instruction is parsed and executed using register emulation with appropriate shifts and updates.

## 💡 Simulation Logic

- `mov Rn,value`: Loads value into register R1 or R2
- `move Rn,left/right`: Performs a circular shift on the register value
- The accumulator is used as the main processing register
- The processor state (PS, PC, TC) is updated per instruction

## ▶️ How to Run

1. Make sure `lab2.TXT` is located at the correct path in the C++ code (e.g., `D://Labaoc2//lab2.txt`)
2. Compile using any C++ compiler:
   ```bash
   g++ -std=c++11 -o processor_sim main.cpp
   ./processor_sim
3. Observe step-by-step execution output in the console.
   
## ⚙️ Features

20-bit register emulation with std::bitset<20>
Status flag logic (PS): +, -, 0
Rotational shift logic for simulating left/right bitwise movement
Instruction parsing and tact counting

## 📘 Learning Objectives

Understand how assembly-like instructions interact with processor architecture
Simulate register-level operations and state changes
Practice bitwise logic and state machine design in C++

