# micro-lafentika![microlafentika wallpaper](https://user-images.githubusercontent.com/59177804/169384741-f5c58f4d-e3a3-492f-b93d-fbd1016cfee6.png)

Designing a 16-bit functional microprocessor with basic operations from scratch with Logisim.  This is solely for academic purposes.

## Table of Contents

* [Overview](#overview)
* [Installation](#installation)
* [Hardware Specification](#hardware-specification)
    * [Overview](#overview)
    * [ALU](#ALU)
    * [Registers](#Register-File)
    * [Memory](#Memory)
    * [Control Unit](#Control-Unit)
    * [Multiplexers](#Multiplexers)
    * [Control Flow](#control-flow)

## Overview

This is an educational project, with the goal of learning and building how microprocessors work at a low level
by implementing a complete, functional 16 bit computer in Logisim.  

 - How many instructions? - 16 instructions

 - How many registers? - 16 16-bit registers

 - What size of processor? - 16-bit microprocessor

 - What size of instructions? - 16-bit size instructions

 - What architecture? - Harvard Architecture. 

| ALU      | Branch       | Memory|
 :----------  |:------------:|:------------:|
|Add|Beq|Load|
|Sub|Bne|Store|
|Mul|Jump|
|Div|
|Two's Complement|
|XOR|
|AND|
|OR|
|ORi|
|ANDi|
|ADDi|

 
 - Format of instructions - 

 <p>Sample DataPath Image</p>  

![ALU Data Path](https://raw.githubusercontent.com/kwabenadarkwa/micro-lafentika/master/data%20path%20for%20ALU%20instructions.png?token=GHSAT0AAAAAABI4XEQ2IFWOVSK3YPRHN3XOYT5FZBA)

## Installation

Install Logisim, following instructions at http://www.cburch.com/logisim/. 

The entire computer is contained in main.circ.

# Objectives in order of execution:
- [x] Arithmetic Logic Unit  
- [x] Control Unit
- [x] Register file
- [x] Data Path
# Data Path  

# ALU (Arithmetic & Logic Instructions)
- [x] Addition : 0000
- [x] Subtraction : 0001
- [x] Multiplication : 0000
- [x] Divider : 0011
- [x] AND : 0100
- [x] OR : 0101
- [x] XOR : 0110
- [x] Negation : 0111
- [x] ADDi : 1011
- [x] ORi : 1110
- [x] ANDi : 1111

The ALU generates three outputs; the output of an ALU operation, a branch equal signal and a branch not equal signal

# Register-File
The register file contains registers that are 16-bit and capable of keeping data for operations in
the processor

# Memory
- [x] Branch Equal(BEQ) : 1000
- [x] Branch Not Equal (BNE) : 1001
- [x] Jump : 1010
- [x] Load : 1100
- [x] Store : 1101

# Control-Unit
The control unit accepts four inputs and outputs 11 control signals to be used by the rest of the processor.
The four inputs are Bits 15, 2,1,0.


# Multiplexers
There are 4 main multiplexers:  
**Labeled MUX1**: This multiplexer is for selecting whether the data needed to write to the register file is from an ALU output or a load operation from memory into register file  
**Labeled MUX2**: This multiplexer is for selecting between a load or a store operation. It is used to determine what operands to use as the instruction formats for load and store differ between where memory and register are located.  
**Labeled MUX3**: This multiplexer is used when we are performing either an immediate or a basic ALU operation. Basic ALU operations use data from the register and immediate operations use constant values specified in the instruction.  
**Labeled MUX4**: This multiplexer selects whether an operation is a JUMP, BRANCH EQUAL, BRANCH NOT EQUAL.

# Control-Flow
This describes how programs react when they meet a condition.

# Instructions for Contributors
- The initial designs are organized into one folder.
- New designs should be added to the [main.circ](./main_designs/main.circ) in the [main_designs](./main_designs/) directory.
- The main.circ Logisim file has sub-circuits for ALU, register_file, CU.
- We'll do all our circuit designs in there.
- Let's get some work done

 - Format of instructions : 

ALU 
|   15   | 14 -11      | 10 - 7|6-3|2|1-0|
 :----------  |:------------:|:------------:|:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations |Destination Register Address|Source Register 2 Address|Source Register 1 Address|Bit to detemine between Logic or Arithmetic Operations|Particular Operation|

Sample ALU Instruction: 0090h - Add reg0, reg 1, reg 2(Add value in register 1 to register 2 and store it in register 0).


Store 
|   15   | 14 - 7      | 6 - 3|2 - 0|
 :----------  |:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations |Selecting RAM Address|Register Address from which data is sourced|Selecting whether it is a Load/Store Operation|Selecting whether it is a Load/Store Operation|Selecting whether it is a Load/Store Operation| 

Sample Store Operation: 8005h - STR r0, [r0] (Store value in register 0 (0000) in 8-bit RAM Address stored in r0 )





Load 
|   15   | 14 - 11      | 10 - 3|2 - 0|
 :----------  |:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations | Register Address |Address for data in RAM |Selecting whether it is a Load/Store Operation|  

Sample Load Operation: c004h -  LDR r4, [r0] (Load from 8 bit RAM Address in register 0 (0000) into register 4(0100) )




### The Branch Component


Instruction Formats:

Branch Equal
|   15   |14-11 | 10 - 7      | 6 - 3|2 - 0|
 :----------  |:------------:|:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations |Offset |Register address with second operand to compare|Register address with first operand to compare|Opcode for Beq operation|

Sample Branch-equal instruction:  E9A0 - Beq reg3,reg4, -3 (check the contents of register 3 and 4, if equal move two step back from 
the current instruction)


Branch Not Equal
|   15   |14 - 11   | 10 - 7    | 6 - 3|2 - 0|
 :----------  |:--------------:|:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations |Offset |Register address with second operand to compare|Register address with first operand to compare|Opcode for Bne operation|



Jump
|   15   |14 - 12   | 10 - 3|2 - 0|
 :----------  |:--------------:|:------------:|:------------:|
|Selecting between ALU and the other operations | Unused |New address in instruction memory to jump to |Opcode for Jump operation|

Find the DataPaths for the various units in the presentation document.



You might want to read the post Machu wrote on building [MicroL'afentika](https://machugram.netlify.app/posts/student/building-microlafentika-2022.html)
