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
** CONCEPT: **
<br>
<img width="3054" height="2176" alt="alui description" src="https://github.com/user-attachments/assets/5aa0d54a-ac02-4d4b-9d1d-011b79b4b16d" />
<br>
## Registers: 
A single-bit register, which we call Bit, or binary cell, is designed to store a single bit
of information (0 or 1). The chip interface consists of an input pin that carries a data
bit, a load pin that enables the cell for writes, and an output pin that emits the current state of the cell.
<br>
<img width="492" height="92" alt="image" src="https://github.com/user-attachments/assets/98fac92b-f86a-4554-890f-034fa7aaa8fa" />
<br>

## Memory:

<br>
A direct-access memory unit, also called RAM, is an array of n w-bit registers,
equipped with direct access circuitry.
<br>
<img width="185" height="228" alt="image" src="https://github.com/user-attachments/assets/3aeba0a7-21cc-40b8-818a-4c61ccf610ad" />
<br>

## Program Counter: 
<img width="286" height="106" alt="image" src="https://github.com/user-attachments/assets/60251831-1f33-4738-a784-7e50beb6351f" />
<br>
A counter is designed to contain the address of the instruction that the computer should fetch and execute next. A counter has to simply increment itself by 1 in each clock cycle, causing the computer to fetch the next instruction in the program. In other cases, for example, in
‘‘jump to execute instruction number n’’ we want to be able to set the counter to n.

### Circuit: 
<img width="800" height="610" alt="image" src="https://github.com/user-attachments/assets/95cb2a34-c0b9-40d7-8448-e176623fb41a" />
<br>
>CPU execution unit, where it takes varous instructions and their sets and perform the execution. A-register and D-registers are also used in this segment to implement A-instructions and C-instructions.
<br>
<img width="803" height="610" alt="image" src="https://github.com/user-attachments/assets/0780d49e-e759-4ce0-b84d-b5a108ad5f29" />








## Credits
This project is based on the Nand2Tetris course by Noam Nisan and Shimon Schocken, who developed the Hack platform and provided the test infrastructure.
