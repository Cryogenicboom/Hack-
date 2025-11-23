# HACK CHIPSET
### Building CPU from fundamental blocks of digital logics. 
<br>
This repo contains my all hardware implementation of the Hack Computer as specified in the Nand2Tetris course. Every component from elementary logic gates up to the CPU, RAM, and PC—is built from NAND gates in HDL. This project will help you understand digital logic, CPU datapath design, control logic, and how instructions map to hardware.

## Architecture Summary
**1. Instruction Set**
The Hack CPU supports two instruction types:
> 1. A-instruction (@value): Loads a constant or address into the A register.
> 2. C-instruction (dest=comp;jump): Performs ALU computation using A and D registers, writes results to destinations, and triggers conditional jumps.
<br>

**2. CPU Components Implemented**
> A-Register: Holds addresses and immediate values.
> D-Register: General purpose data register.
<br>

**3. ALU**
> Supports arithmetic and logic operations like (add, sub, and, or, not, negate, zeroing, increment, etc.) based on 6 control bits.
<br>

**4. Program Counter (PC)**
> Increments sequentially unless a jump is triggered.
<br>

**5. Control Logic**
> Decodes instruction bits to control ALU inputs, memory writes, PC load, and register updates.
<br>

**6. Memory System**
memory system consist of:
> RAM16K <br>
> Screen memory (16384 bytes) <br>
> Keyboard memory-mapped register <br>

**Memory is muxed and accessed using the A register and control signals from the CPU.**

## ALU implementation: 
**CONCEPT: **
<br>
<img width="3054" height="2176" alt="alui description" src="https://github.com/user-attachments/assets/5aa0d54a-ac02-4d4b-9d1d-011b79b4b16d" />




## Credits
This project is based on the Nand2Tetris course by Noam Nisan and Shimon Schocken, who developed the Hack platform and provided the test infrastructure.
