# Workshop on RISC-V based Microprocessor

## Table of Contents
* [Introduction of RISC-V Instruction Set Architecture](#Introduction-of-RISC-V-Instruction-Set-Architecture)
* [Why we use RISC-V](#Why-we-use-RISC-V)
* [Day-1 Introduction to RISC-V ISA and GNU Compiler Toolchain](#Day-1-Introduction-to-RISC-V-ISA-and-GNU-Compiler-Toolchain) 
    * [Program Counter](#Program-Counter) 
    * [Fetch](#Fetch)
    * [Decode](#Decode)
    * [Execute](#Execute)
    * [RISC-V Pipelined Core](#RISC-V-Pipelined-Core)
* [Conclusion](#Conclusion)
* [Acknowledgements](#Acknowledgements)
* [References](#References)

## Introduction of RISC-V Instruction Set Architecture

RISC-V is a free and open source ISA which is based on reduced instruction set computer (RISC) principles. RISC-V ISA is enabling a new era of processor modernity through open standard collaboration.

### Why we use RISC-V?
- Open-source
- Simple
- Small Standard base ISA
- Avoids technology dependent features
- Flexible for anyone at almost zero cost

## Day-1 Introduction to RISC-V ISA and GNU Compiler Toolchain

ISA is nothing but the language of the computer. This is a way we are going to talk to the computers. For example, if you have a C program and if you want to run this C program on a hardware, then this particular C program first compiled in its assembly language program or RISC-V assembly language program. This assembly language program is then converted into the machine language program which is understood by the hardware of the computer. 

### C program to find the sum of numbers from 1 to n

#### Compile using GNU toolchain
- First, we open up the leafpad to write our C program
![](/images/c.png)
- Then, we write the following program to evaluate the sum of numbers from 1 to n.
![](/images/c.png)
- Then we compile the program using GNU compiler
![](/images/c.png)
- Lastly, we run the compiled object file
![](/images/c.png)

#### Using RISC-V compiler toolchain, code disassemble and spike simulator
- Now we run the **sum1ton.c** file using RISC-V simulator:
![](/images/c.png)
- To see the assembly code for the C program, first we open up the new tab and type the following command: 
![](/images/c.png)
  This is the output of the objdump file using O1 switch.
![](/images/c.png)
- To run the object file we are using the spike simulator:
![](/images/c.png)

#### Debugging using RISC-V Simulator
- To debug the assembly set instructions, we are using the spike debugger:
![](/images/c.png)
- We open up a new tab in the same terminal window and look for the address loaction of the pc.
- After invoking the spike debugger we type the following command to run until pc 100b0:
![](/images/c.png)
- To see the contents of the register a0, we type *reg 0 a0*:
![](/images/c.png)
  Press **enter** to execute the next set of assembly code instructions
  ![](/images/c.png)
  ![](/images/c.png)

### C program of unsigned and signed number representation

#### Unsigned Number Representation
- Write the C program for unsigned number representaion
![](/images/c.png)
- To compile the unsignedHighest.c we use the following command
![](/images/c.png)
- To view the output of the unsignedHighest.c program we invoke the spike simulator
![](/images/c.png)

#### Signed Number Representation
- Write the C program for signed number representaion
![](/images/c.png)
- To compile and view the signedHighest.c we use the following commands:
![](/images/c.png)
