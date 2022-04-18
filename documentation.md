# Official Documentation For Project
### WHAT IS THIS PROJECT?
This is a microprocssor built based on the RISC and Harvard Architectures.
The RISC architecture was selected because it is a type of microprocessor architecture that utilizes a small, highly-optimized set of instructions rather than the highly-specialized set of instructions typically found in other architectures.

The Harvard architecture is preferred because an instruction is executed in a single cycle and also CPU can access instructions and read/write at the same time.

Using the Harvard architecture, there are mainly two types of memory to deal with, Instruction and Data Memory. 
The instruction memory stores the current instruction. It relies on the program counter to select the next instruction.
The data memory stores the operands, register locations and operations required for an instruction operation.

### THE REGISTER FILE

- What is a register file?  

A register file is a component that has a structure of multiple registers that are used for loading values.  

How many registers? - 16 registers  

How many ports? - 9 ports.   
1 select line. 1 enable line , 4 input lines [1 write address port, 1 write data port, 2 register address ports ] , 2 register data ports  

Clock input and output  


### THE Arithmetic Logic Unit
Two Inputs
Select Lines
No Of Bits


#### Components of ALU
-  Addition : 00
-  Subtraction : 01
-  Multiplication : 10
-  Divider : 11
-  AND : 00
-  OR : 01
-  XOR : 10
-  Negation : 11


Instruction Formats:

|1|4|4|4|1|2
 :----------  |:------------:|:------------:|:------------:|:------------:|:------------:|
| Category      | rd       | rs1|rs2|A/L|ALUCP|

Sample ALU Instruction: 0090h - Add reg0, reg 1, reg 2(Add value in register 1 to register 2 and store it in register 0).

Control Unit*
-


### THE Memory Component


Instruction Formats : 

Store 
|   15   | 14 - 7      | 6 - 3|2 - 0|
 :----------  |:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations |Selecting RAM Address|Register Address from which data is sourced|Selecting whether it is a Load/Store Operation| 

Sample Store Operation: 8005h - STR r0, [r0] (Store value in register 0 (0000) in 8-bit RAM Address stored in r0 )





Load 
|   15   | 14 - 11      | 10 - 3|2 - 0|
 :----------  |:------------:|:------------:|:------------:|
|Selecting between ALU and the other operations | Register Address |Address for data in RAM |Selecting whether it is a Load/Store Operation|  

Sample Load Operation: c004h -  LDR r4, [r0] (Load from 8 bit RAM Address in register 0 (0000) into register 4(0100) )




### The Branch Component


Instruction Formats.




### Memory 
Load :
The load instruction is an instruction that retrieves data from the memory and stores it in the register file.


Store: 
The store instruction is an instruction that retrieves data from the register file and stores it in the memory.



### DATA PATH
Datapath is the path that the input data follows in a processor to appear as an output. 




