# RISC-V Pipelined Processor with Hazard Unit

## Project Overview
This project represents an evolution of my single-cycle processor into a more sophisticated pipelined processor. The enhancement includes the integration of a Hazard Unit, fundamentally transforming the processor to efficiently handle data dependencies, memory read stalls, and pipeline flushing for branch instructions. The goal is to optimize the execution flow by eliminating the need for `nop` instructions, thus allowing the pipeline to operate at its highest potential efficiency.

## Evolution and Features
- **From Single-Cycle to Pipelined:** This iteration builds upon the foundation of the single-cycle processor, extending its architecture into a 5-stage pipelined design.
- **Hazard Unit Integration:** A major addition to this version is the Hazard Unit, which autonomously addresses hazard conditions to improve data flow and instruction execution within the pipeline.
- **Optimized Execution Path:** By managing data hazards, control hazards, and stalling conditions, the processor now circumvents the previously necessary `nop` instructions, facilitating uninterrupted code execution.

## Key Enhancements
- **Data Path Enhancements:** Introduction of new datapath lines and MUXes in the EX stage to enable register forwarding, crucial for resolving data hazards.
- **Automatic Hazard Management:** The Hazard Unit identifies and resolves pipeline hazards through register forwarding, stalling, and flushing, ensuring seamless instruction execution.
- **Improved Pipeline Efficiency:** With mechanisms to handle various types of hazards, the processor minimizes delays and maximizes throughput, significantly enhancing overall performance.

## Project Components
Included in this project are:
- **Pipelined Processor Implementation (`project07.dig`):** The top-level processor design featuring the newly added Hazard Unit.
- **Comprehensive Hazard Unit:** Central to this project, designed to optimize performance by efficiently managing pipeline hazards.
- **Targeted Test Cases:** Specifically designed programs to test the processor's capability to automatically handle different hazard scenarios without manual `nop` instructions.
- **Auxiliary Circuits and Files:** Supporting components including RAM modules for `lw` and `sw`, an ASCII-based disassembler, and the necessary decoder logic.

## Development Tools
- **Digital:** Circuit design and simulation https://github.com/hneemann/Digital

## Top Level Circuit:
![image](https://github.com/mvvillarrealblozis/Pipelined-RISC-V-Processor/assets/112027248/b8988e92-16b4-40f4-8713-25c598a4dcc0)
