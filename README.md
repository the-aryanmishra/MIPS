
# MIPS Assembler and Processor Simulation

## Overview
This repository contains two primary components:
1. **Assembler**: Converts MIPS assembly code (MARS format) into machine code.
2. **Processor Simulation**: Simulates both pipelined and non-pipelined processors using Python. The processor executes machine code for the bubble sort and factorial algorithms.

---

## Features
### 1. Assembler
- **Purpose**: Converts MIPS assembly code to machine code.
- **Key Details**:
  - Supports R-type, I-type, J-type, LW/SW instructions.
  - Handles pseudo-instructions (`move`, `bgt`) by translating them into valid MIPS instructions.
  - Performs two-pass assembly:
    - **First Pass**: Collects labels and their memory addresses.
    - **Second Pass**: Converts instructions into machine code.
  - Outputs machine code in a file named `machine_code.txt`.

### 2. Processor Simulation
Simulates execution of the machine code generated by the assembler for the following algorithms:
- **Bubble Sort**: Sorts an array in ascending order.
- **Factorial**: Computes the factorial of a number.

#### Non-Pipelined Processor
- Executes instructions sequentially.
- Includes detailed logging of each step in the execution process.

#### Pipelined Processor
- Implements instruction-level parallelism.
- Simulates stages: Fetch, Decode, Execute, Memory, Write-back.
- Includes hazard detection and forwarding to manage data dependencies.

---

## Files
- `Assembler.py`: Contains the assembler code to generate machine code from MIPS assembly.
- `non-pipeline.py`: Simulates the non-pipelined processor.
- `pipeline.py`: Simulates the pipelined processor.
- `Assignment Report.pdf`: Documentation of the algorithms and implementation details.

---

## Usage
### Running the Assembler
1. Prepare your MIPS assembly code in a file (e.g., `mips.txt`).
2. Run the assembler script:
   ```bash
   python Assembler.py
   ```
3. The machine code will be generated in `machine_code.txt`.

### Running the Processors
#### Non-Pipelined Processor
1. Ensure the `machine_code.txt` file is generated by the assembler.
2. Run the non-pipelined processor simulation:
   ```bash
   python non-pipeline.py
   ```

#### Pipelined Processor
1. Ensure the `machine_code.txt` file is generated by the assembler.
2. Run the pipelined processor simulation:
   ```bash
   python pipeline.py
   ```

---

## Algorithms
### Bubble Sort
- Implemented in MIPS assembly and translated to machine code by the assembler.
- Simulates sorting an array iteratively.

### Factorial
- Computes the factorial of a given number using iterative or recursive logic.

---

## Contributors
- **Divyam Sareen** (IMT2022010)
- **Aryan Mishra** (IMT2022502)
