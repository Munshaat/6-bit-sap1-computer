# SAP-1 Architecture-Based 6-bit Computer

Design and implementation of a **6-bit computer based on the SAP-1 (Simple-As-Possible) architecture**, developed as an Electrical and Electronic Engineering project at the Islamic University of Technology (IUT).

The project involved designing, integrating, and testing the major functional modules of a basic computer system using **Proteus**, including the program counter, memory address register, RAM, instruction register, controller sequencer, accumulator, B register, arithmetic and logic unit, output register, clock, and common bus.

## Project Overview

The objective of this project was to understand the internal operation of a simple computer architecture and implement its major hardware modules at the circuit level.

Each module was initially tested independently using logic states and logic probes before being integrated with the system bus and control circuitry.

The completed system was verified by programming data into RAM and executing operations through the SAP-1 architecture. The final output demonstrated successful **addition and subtraction operations**.

## System Modules

### Program Counter

* Designed and tested the program counter module.
* Connected the program counter output to the system bus.
* Used a **74HC245 buffer** to maintain unidirectional data flow from the program counter to the bus.
* Verified the module using logic states before system integration.

### Memory Address Register (MAR)

* Designed the MAR module and verified its operation using manual connections.
* Connected the MAR to the common bus.
* Sequentially connected the bus bits to the corresponding MAR inputs.

### Random Access Memory (RAM)

* Implemented the RAM module for storing program instructions and data.
* Initially tested a 74LS189 IC, but it did not provide accurate data storage when connected to the bus.
* Replaced it with a **74LS89**, which successfully stored data at the required addresses.
* Configured the RAM for read and write operations.

### Instruction Register

* Designed and tested the instruction register in Proteus.
* Implemented input and output control for transferring instruction data between the bus and register.
* The lower nibble of the stored instruction could be transferred to the bus when the output control was enabled.

### Controller Sequencer

* Designed the controller sequencer to generate the required timing and control signals.
* Tested opcode inputs manually using logic states.
* Verified the activation of control signals during the corresponding T-states.
* Integrated the sequencer with the instruction register after verifying its operation.

### Arithmetic and Logic Unit (ALU)

* Designed the ALU submodule and tested its operation using logic probes and logic states.
* Connected the ALU inputs to the accumulator and B register.
* Integrated the ALU output with the system bus.
* The initial implementation produced incorrect output for certain cases.
* Replacing the **74HC365 buffer with a 74HC245** resolved the output problem.

### Accumulator

* Designed and tested the accumulator module independently.
* Connected the accumulator to the common bus through controlled switching.
* Verified unidirectional data transfer between the accumulator and bus.
* Integrated the accumulator with the ALU.

### B Register

* Designed and tested the B register module.
* Verified the `BI` control signal from the controller sequencer.
* Connected the B register to receive data from the bus and provide data to the ALU.

### Output Register

* Designed and tested the output register using logic states and logic probes.
* Connected the register to the common bus and main SAP clock.
* Used the controller sequencer to control the output operation.
* Verified the final system by executing programmed operations and observing the results.

### Clock

* Designed the main clock circuit used for synchronizing the SAP-1 modules.
* The clock provides the timing required for sequential operations throughout the computer.

## Bus Architecture

The individual modules communicate through a common system bus.

The bus provides controlled data transfer between:

* Program Counter
* Memory Address Register
* RAM
* Instruction Register
* Accumulator
* B Register
* ALU
* Output Register

Buffer ICs and control signals were used to maintain appropriate **unidirectional data flow** between modules.

## Simulation and Verification

Each module was first verified independently before integration.

The general verification process included:

1. Creating the module in Proteus.
2. Applying manual logic states to the inputs.
3. Observing outputs using logic probes.
4. Correcting circuit or component-level issues.
5. Connecting the module to the common bus.
6. Integrating the module with the controller sequencer.
7. Testing the complete SAP-1 system.

For final verification, the RAM was placed in programming mode and input data was stored at specific addresses. The system was then switched to run mode and the clock was enabled. The completed system successfully produced results for **addition and subtraction operations**.

## Hardware / Components

The project involved digital logic ICs and circuit-level components including:

* 74HC245
* 74LS89
* 74HC04
* 74HC173
* Logic states
* Logic probes
* Digital bus connections
* Clock circuit
* Registers and control circuitry

## Tools

* **Proteus**
* Digital logic simulation
* Schematic design
* PCB layout/design

## Project Highlights

* Designed a complete **SAP-1 architecture-based 6-bit computer**.
* Developed and tested individual CPU and memory modules.
* Implemented a common bus architecture for data transfer.
* Designed control and sequencing logic.
* Debugged hardware-level simulation issues.
* Verified unidirectional data flow using buffer ICs.
* Designed PCB layouts for selected modules.
* Integrated the individual modules into a functioning computer system.
* Verified addition and subtraction through the completed system.


## Repository Contents

```text
6-bit-sap1-computer/
│
├── README.md
├── SAP-1 Architecture-Based 6-bit Computer Design and Implementation.pdf
│
└── [Proteus / PCB files, if available]
```

## Academic Project

**Department of Electrical and Electronic Engineering**
**Islamic University of Technology (IUT)**

**Project:** SAP-1 Architecture-Based 6-bit Computer — Design and Implementation
