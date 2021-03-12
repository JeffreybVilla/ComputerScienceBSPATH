# Intro
    Every assembly language is designed for exactly 1 specific computer architecture.
    Assembly code is converted into executable machine code by a utility program referred to as an assembler.
    We will write and execute assembly language programs in Visual Studio environment.
    First section describes statements that are accepted by Visual Studio's assembler.
    The Microsoft Macro Assembler (MASM) is an x86 assembler that uses the Intel syntax for MS-DOS and Microsoft Windows.

# Assembly Language Statements
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20310%20Assembly%20Language/images/assemblyEx1.png)

## Comments
    ; Comments start with semicolon

## Instructions
    3 types of functional assembly language statements: instructions, directives, and macros.
    An instruction is translated by the assembler into 1 or more bytes of object code (machine code) that is executed at run time.
    Each instruction corresponds to 1 of the operations that the 80x86 CPU can perform.

    Above example has 5 instructions (80x86 instructions):
    mov eax, number ;Copies the doubleword in memory at the location identified by number to the EAX register in CPU.
    add eax, 158    ;Adds a doubleword represenation of 158 to the current doubleword in the EAX register.
    mov sum, eax    ;Copies the doubleword in the EAX register to the doubleword in memory identified by sum.
    mov eax, 0      ;Exit to operating system
    ret             ;Exit to operating system

## Directives





















# 32-Bit Example using Debugger

# Data Declarations

# Instruction Operands

# Complete 32-Bit Example Windows Input/Output

# Input/Output & Data Conversion Using Macros Defined in IO.H

# 64-Bit Examples

# Summary
