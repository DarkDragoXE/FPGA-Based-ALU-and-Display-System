# FPGA-Based ALU and Display System

This project implements projects like a modular **FPGA-based Arithmetic Logic Unit (ALU)** using **Verilog HDL**, capable of performing arithmetic operations, FIR filtering, safe code verification, and result display through 7-segment multiplexing. Designed and tested on a **Basys 3 (Artix-7)** board.

---

## Features
- **Addition/Multiplication Unit:** Dual 4-bit input arithmetic with display toggle.
- **FIR Filter:** 3-tap [1,2,1] filter implemented for signed 8-bit signal processing.
- **Safe Code Verification:** 4-bit comparator system with XOR and inversion logic.
- **BCD to 7-Segment Driver:** Converts 4-bit BCD to display patterns on 7-segment display.
- **LED Counter:** Clock-driven visual activity monitor.

---

## Modules Overview
| Module | Function |
|---------|-----------|
| `SevenSegmentDisplay.v` | Displays operands and results on 7-segment display |
| `TopModule.v` | FPGA top integration for arithmetic logic |
| `fir_filter.v` | Implements a 3-tap FIR digital filter |
| `safesys.v` | 4-bit secure input comparison module |
| `safesystb.v` | Testbench for safesys |
| `BCD7seg.v` | Converts 4-bit input to 7-segment encoding |
| `top.v` | Top wrapper integrating decoder and LED counter |

---

## Hardware Setup
- **FPGA Board:** Basys 3 (Artix-7 XC7A35T)
- **Clock:** 100 MHz onboard oscillator
- **Switch Inputs:** Used for operands A and B
- **Toggle Switch:** Switches between Addition/Multiplication
- **7-Segment Display:** Shows input and output results
- **LEDs:** Indicate counter state and operation activity

---

## Toolchain
- **Language:** Verilog HDL  
- **Software:** Xilinx Vivado 2023.1  
- **Simulation:** Vivado Simulator  

---

## Repository Structure
