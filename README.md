# micro-lafentika
Designing a 16-bit functional microprocessor with basic add,subtract,multiply,and,or operations from scratch with Logisim.  

# Decisions 
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

 - How many instructions? - 12 instructions

 - How many registers? - 16 registers

 - What size of processor? - 16-bit microprocessor

 - What size of instructions? - 16-bit size instructions

 - What architecture? - Harvard Architecture
 
 - Format of instructions - 

 <p>Sample DataPath Image (We have to build ours):</p>  

![DataPath](https://docsdrive.com/images/ansinet/itj/2007/fig3-2k7-497-508.gif)    

# Objectives in order of execution:
- [ ] Data Path
- [ ] Arithmetic Logic Unit  
- [ ] Control Unit
- [ ] Registers
- [ ] Buses

# Data Path  


# Arithmetic Logic Instructions
- [x] Addition
- [x] Subtraction
- [ ] OR
- [ ] AND
- [x] Multiplication
- [x] Ripple Adder [Contains both addition and Subtraction]

# Control Unit


# Registers


# Buses



# Currently on...
- [ ] ALU
- [ ] Data Path


# Instructions for Contributors
- The initial designs are organized into one folder.
- New designs should be added to the [main.circ](./main_designs/main.circ) in the [main_designs](./main_designs/) directory.
- The main.circ Logisim file has sub-circuits for ALU, register_file, CU.
- We'll do all our circuit designs in there.
- Let's get to work

| Category      | rd       | rs1|rs2|A/L|ALUCP|
 :----------  |:------------:|:------------:|:------------:|:------------:|:------------:|
|1|4|4|4|1|2
