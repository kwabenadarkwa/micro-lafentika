# Official Documentation For Project
### WHAT IS THIS PROJECT?
This is a microprocssor built based on the RISC and Harvard Architectures.
The RISC architecture was selected because it is a type of microprocessor architecture that utilizes a small, highly-optimized set of instructions rather than the highly-specialized set of instructions typically found in other architectures.

The Harvard architecture is preferred because an instruction is executed in a single cycle and also CPU can access instructions and read/write at the same time.

Using the Harvard architecture, there are mainly two types of memory to deal with, Instruction and Data Memory. 
The instruction memory stores the current instruction. It relies on the program counter to select the next instruction.
The data memory stores the operands, register locations and operations required for an instruction operation.

REQUIREMENTS & PARAMETERS
 How many instructions? - 16 instructions

 - How many registers? - 16 16-bit registers

 - What size of processor? - 16-bit microprocessor

 - What size of instructions? - 16-bit size instructions

 - What architecture? - Harvard Architecture. 

### THE REGISTER FILE

- What is a register file?  

A register file is a component that has a structure of multiple registers that are used for loading values.  

How many registers? - 16 registers  

How many ports? - 9 ports.   
* 1 select line. 
  * Has bits used to select a register to read from and write to.
* 1 enable line  
  * Responsible for enabling the writing of data to a register file.
* 4 input lines [1 write address port, 1 write data port, 2 register address ports ] 
  * The write address port has bits which specifies a particular register file to write to. The write data port contains bits to be written to selected   register. The two register address ports contain bits to specify registers to work on.
* 2 register data ports  
  * They contain data read from selected regiters.

Clock input and output  


### THE Arithmetic Logic Unit
Two Inputs
Select Lines
Number Of Bits


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




### Memory 
Load :
The load instruction is an instruction that retrieves data from the memory and stores it in the register file.


Store: 
The store instruction is an instruction that retrieves data from the register file and stores it in the memory.



### DATA PATH
Datapath is the path that the input data follows in a processor to appear as an output. 




