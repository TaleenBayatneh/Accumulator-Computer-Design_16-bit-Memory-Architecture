# 16-bit Accumulator Computer - Verilog Implementation

## Project Overview
This Verilog HDL project implements a functional 16-bit accumulator-based computer architecture, designed as part of the Computer Organization and Microprocessor course at Birzeit University. The system embodies Von Neumann architecture principles with a focus on accumulator-centric operations, featuring a complete implementation of the instruction cycle (fetch-decode-execute) and memory subsystem.

## Technical Specifications
- **16-bit Data Path**: All registers and memory operations use 16-bit architecture
- **Key CPU Components**:
  - Accumulator (AC) - Primary arithmetic register
  - Program Counter (PC) - Instruction pointer
  - Instruction Register (IR) - Current operation storage
  - MAR/MBR - Memory interface registers
- **Memory System**: 16-bit addressable memory with dedicated instruction/data segments
- **Instruction Set**: Supports fundamental operations including:
  - Arithmetic: ADD, SUB, MUL, DIV
  - Memory: LOAD, STORE
  - Control: Conditional branching (future extensibility)

## Implementation Highlights
1. **Modular Design**: Separated CPU, memory, and register files for clean hierarchy
2. **Verified Operations**:
   - Basic arithmetic expression evaluation
   - Complex computation: Y = (A+B+C-5)/(D+E+1)
3. **Comprehensive Testing**:
   - Memory initialization verification
   - Instruction execution waveforms
   - Result validation at designated memory locations

## Sample Execution
```assembly
Memory Initialization:
Address 0: 0x180A (LOAD [10])
Address 1: 0x580B (MUL [11])
Address 2: 0x3005 (ADD #5)
Address 3: 0x280C (STORE [12])

Data:
Address 10: 9 (0x0009)
Address 11: -4 (0xFFFC)

Execution Result:
(9 × -4) + 5 = -31 → Stored at Address 12
