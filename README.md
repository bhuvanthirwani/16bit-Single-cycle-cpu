# 🖥️ 16-bit Single Cycle CPU

> **A Verilog Implementation of a Custom 16-bit Processor Architecture**

This project implements a fully functional **16-bit Single Cycle Central Processing Unit (CPU)** using **Verilog HDL**. It is designed to execute instructions in a single clock cycle, demonstrating the fundamental principles of computer architecture and digital logic design.

---

## 🛠 Tech Stack

| Component | Technology |
| :--- | :--- |
| **HDL** | ![Verilog](https://img.shields.io/badge/Verilog-HDL-B02927?style=flat&logo=verilog) |
| **Simulation** | ModelSim / Vivado / Icarus Verilog |

---

## 🏗 Architecture Overview

The CPU consists of several key modules working in unison to fetch, decode, and execute instructions:

*   **Logic Unit (ALU)**: Performs arithmetic and logical operations (`ALU_Unit.v`).
*   **Control Unit**: Generates control signals based on the instruction opcode (`Control_Unit.v`).
*   **Data Memory**: Stores data for load/store operations (`Data_Memory.v`).
*   **Program Counter (PC)**: Keeps track of the current instruction address.
*   **Multiplexers**: Handles data routing (e.g., `ALUinput_Mux.v`, `Branch_Mux.v`).
*   **Sign Extenders**: Handles immediate values (`ImmExtend_Branch.v`).

### Top-Level Module
The `CPU_16_Top.v` module integrates all sub-components, connecting the data path and control path to form the complete processor.

---

## 📂 File Structure

```text
/
├── CPU_16_Top.v        # Top-level entity
├── ALU_Unit.v          # Arithmetic Logic Unit
├── Control_Unit.v      # Main Control Unit
├── Data_Memory.v       # RAM / Data Storage
├── PC.v / Program...   # Program Counter
├── Adder.v             # Adder for PC increments
└── ...
```

---

## 🚀 Key Features

-   **Single Cycle Execution**: Each instruction completes in one clock cycle.
-   **16-bit Data Path**: Handles 16-bit logical and arithmetic operations.
-   **Branching & Jumping**: Supports flow control via conditional branches and jumps.
-   **Modular Design**: Clean separation of concerns with distinct Verilog modules.

---

## ⚡ Usage

1.  **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/16bit-Single-cycle-cpu.git
    ```

2.  **Open in Simulator**
    Load the `CPU_16_Top.v` and its dependencies into your preferred Verilog simulator (e.g., ModelSim, Vivado).

3.  **Run Testbench**
    Compile and run `CPU_TOP_test.v` to verify the processor's functionality.

---

*Designed for educational exploration of Computer Architecture.*
