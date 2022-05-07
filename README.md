# micro-lafentika
Designing a 16-bit functional microprocessor with basic add,subtract,multiply,and,or operations from scratch with Logisim.  

## Table of Contents

* [Overview](#overview)
* [Installation](#installation)
* [Hardware Specification](#hardware-specification)
    * [Overview](#overview)
    * [Registers](#registers)
    * [ALU](#alu)
        * [Codes](#codes)
        * [Read/Write Location](#readwrite-location)
        * [ALU Control](#alu-control)
* [Todo](#todo)


## Overview

This is an educational project, with the goal of learning and building how microprocessors work at a low level
by implementing a complete, functional 16 bit computer in Logisim.  

 - How many instructions? - 12 instructions

 - How many registers? - 16 registers

 - What size of processor? - 16-bit microprocessor

 - What size of instructions? - 16-bit size instructions

 - What architecture? - Harvard Architecture. 

| ALU      | Branch       | Memory|
 :----------  |:------------:|:------------:|
|Add|Beq|Load|
|Sub|Bne|Store|
|Mul|
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

  ![Screenshot 2022-03-18 152257](https://user-images.githubusercontent.com/59177804/159033894-b56d2c79-9f1f-481b-a181-a6140a44f9d1.png)


## Installation

Install Logisim, following instructions at http://www.cburch.com/logisim/. 

The entire computer is contained in main.circ.

# Objectives in order of execution:
- [ ] Data Path
- [x] Arithmetic Logic Unit  
- [ ] Control Unit
- [ ] Register file

- [ ] Buses

# Data Path  


# Arithmetic & Logic Instructions
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



# Memory Instructions
- [x] Branch Equal(BEQ) : 1000
- [x] Branch Not Equal (BEQ) : 1001
- [x] Jump : 1010
- [x] Load : 1100
- [ ] Store : 1101

<!--            - - - 1. Arithmetic ---------|
         |
         |
         |
         |
         |
ALU ------  -->



# Control Unit


# Registers


# Buses



# Instructions for Contributors
- The initial designs are organized into one folder.
- New designs should be added to the [main.circ](./main_designs/main.circ) in the [main_designs](./main_designs/) directory.
- The main.circ Logisim file has sub-circuits for ALU, register_file, CU.
- We'll do all our circuit designs in there.
- Let's get some work done

 - Format of instructions : 

| Category      | rd       | rs1|rs2|A/L|ALUCP|
 :----------  |:------------:|:------------:|:------------:|:------------:|:------------:|
|1|4|4|4|1|2


|      |       | ||||
 :----------  |:------------:|:------------:|:------------:|:------------:|:------------:|
||||||
