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
- [x] Addition : 00
- [x] Subtraction : 01
- [x] Multiplication : 10
- [x] Divider : 11
- [x] AND : 00
- [x] OR : 01
- [x] XOR : 10
- [x] Negation : 11

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
