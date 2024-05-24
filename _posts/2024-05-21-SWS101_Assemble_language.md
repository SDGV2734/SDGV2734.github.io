---
Title: x86-64 Assembly 
categories: [SWS101, Journal 6 ]
tags: [SWS101]
---

### Learning x86-64 Assembly

**What is asseemble Language?**

An assembly language is a low-level programming language that communicates with the hardware of a computer directly. It allows a software developer to code using words and expressions that can be easier to understand and interpret than the binary or hexadecimal data the computer stores and reads

![Alt text](../image/assemble_t.png)

x86-64 assembly language is a human-readable version of this machine code. It is a low-level programming language that provides direct access to the hardware and allows for highly efficient execution of programs. It uses mnemonics to represent CPU instructions, which are translated into machine code during the compilation process.

#### Getting the tools 

**1. Assembler**

The assembler on the other hand is an important component of assembly programming, as it compiles the assembly code into machine code. In the process of development for x86-64, it is advised to use Flat Assembler (FASM) because the language itself is very intuitive and easy to comprehend and the number of features provided by FASM is more than enough for most of the tasks needed to be accomplished.

**2. Debugger** 

Assembly programming requires an efficient approach to debugging as a way of identifying and fixing errors in the programs that are developed. Being itself a powerful Win32/x86-64 compatible debugger, WinDbg offers a viewpoint on program flow, memory, and registers that is invaluable to assembly programmers.

**3. Installing the Necessary Software**

On the browser we can access the official FASM website where downloads may be made, and the application installed.

We can get WinDbg either from the Windows 10 SDK or get the standalone version which is much better because we don’t want those SDK extras.

**Understanding the Basics**

- The Instruction Set Architecture (ISA): The discrete operations that the ISA defines indicates the operations that a CPU can perform. The x86-64 architecture is an additional development of the traditional x86 architecture with some additional features which make it suitable for 64-bit processing that enables it to access larger memory resources as compared to the other versions of the x86 architecture.

- Registers: Registers are small and furnished storage locations integrated within the CPU. Added new in the x86-64 architecture are 16 general purpose registers, each 64-bit in size which offer more efficient means of computing and data manipulation.

- Memory Model: x86-64 architecture employs linear memory model, so each address begins from 0. This linear memory model is easier to manage compared to the other memory models that were used in previous architectures, namely segmented memory.

### Writing our First Program

#### Setting Up the Development Environment

1. To start programming with FASM, open FASM and create a new file in which you will enter our program code.

2. Compose a Simple Program that includes loading and then termination of the program with a brief commentary to the code.

#### Using WinDbg to Debug Your Program

1. Before starting with debugging launch your program in WinDbg and then see how it initiates its execution steps.

2. It is highly recommended to utilize the Breakpoints, and Single-Step Execution to analyze the program’s behavior deeper.

### Advanced Concepts

The Portable Executable (PE) Format: The Portable Executable (PE) Format:

General information about the PE format is essential when learning how to develop intricate applications. This involves general management of imports and exports, as well as the organization of codes and data sections.

Calling Conventions:

Like any other calling conventions, it is crucial to understand how the Microsoft x64 calling convention works. It determines how functions receive arguments, and how and on which register/effective address it returns a value which in turn affects the structure of assembly code you create.

#### Summary 

Learning x86-64 assembly programming is unique experience because it requires the understanding of the theory coupled with the practical usage. By starting with first principles, then intermediaries, and finally delving deeper into core mechanisms, you’ll have a complete understanding of how software works at its core. That is why it is very important to practice and also try one’s creativity in assembly as the only way to succeed.

#### Overview

Coding with assembly language with one of the generated x86 family’s processors in 64-bit mode. It has been quite interactive to touch such low levels and to learn about the basic operating principle of processors & memory. In general, the tutorial started with architecture – the CPU contains a set of registers that act as small temporary storage spaces of information, and can retrieve data from them with particular instructions or move numbers from or to the main memory. This way I got reminded that rax, rbx, rcx etc. are special purpose registers and i also realized that even accessing the lower parts of these registers should be possible.

To summarize the lessons that I have learned from this topic, I would like to note the following: The information that I have learned in higher level languages such as C/C ++ about stack pointer register RSP, as well as the instruction pointer register RIP, was interesting, but I had no idea how these registers were updated and used in ASM. There are a few things more that seemed quite fresh, the rflags register which contains condition flags and may cause execution included. I had to copy the assembly program above into this file and hit the cycle of debugging it, but all this was the best starting point for consolidating all the concepts. Observing what is happening or what occurs and watching the values changing in the register was particularly beneficial for the process.

The real issue was not knowing how to put together the import table correctly so that windows could import assembly code that used ExitProcess and other things. This tutorial was on the structure of the Portable Executable format and how specific to the situation the import directory table and import address tables can be shaped. There is actually the wisdom acquired that one has to distinguish between the use of registers vs the stack for passing arguments, and this is in connection with the 64-bit calling convention rule.

In the next tutorials, I am much looking forward to elevating it higher still to be able to learn much more about other programs, system calls, calling conventions, and even many others low-level aspects. To be clear, I’m not going to be frequently assembling code as part of writing uncomplicated programs, so Assembly is proving to be this simple language that serves as a connector between the operations of other programming languages and what everything else gets compiled to. It enables user to use computer in a certain way with mind-set at this basic level of things like processor architecture, memory management, stack and calling conventions.

