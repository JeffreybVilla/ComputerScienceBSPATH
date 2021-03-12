# Intro
    Every assembly language is designed for exactly 1 specific computer architecture.
    Assembly code is converted into executable machine code by a utility program referred to as an assembler.
    We will write and execute assembly language programs in Visual Studio environment.
    First section describes statements that are accepted by Visual Studio's assembler.
    The Microsoft Macro Assembler (MASM) is an x86 assembler that uses the Intel syntax for MS-DOS and Microsoft Windows.

# 3.1 Assembly Language Statements
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
    A directive tells the assembler to take some action. 
    Typically doesn't cause machine code to be generated

    Above Example:
    .586             ;tells the assembler to recognize 80x86 instructions that use 32-bit operands.

    .MODEL FLAT      ;tells the assembler to generate code for flat memory model execution.

    .STACK 4096      ;tells the assembler to generate a request to the operating system to reserve 4096 bytes for the system stack.
                     ;the system stack is used at execution time for procedure calls and local storage.
                     ;a stack with 4096 bytes is large enough for most programs.

    .DATA            ;tells the assembler that data items are about to be defined in a data segment.
                     ;Each DWORD directive tells the assembler to reserve a doubleword of memory for data.

    .CODE            ;tells the assembler that the next statements are executable instructions in a code section.

    PROC             ;marks the beginning of a procedure.
    ENDP             ;marks the end of a procedure.
    END              ;tells the assembler to stop assembling statements.

    The label main on the PROC & END directives, names the procedure.
    In the console32 environment, you must call your procedure main.

## Macros
    Each is "shorthand" for a sequence of other statements -- instructions, directives, or even other macros.

    The assembler expands a macro to the statements it represents, and then it assembles these new statements.


## Identifiers
    Formed from letters, digits, and special characters.

    An identifier may not begin with a digit.

    An identifier may have up to 247 characters.

    Restricted identifiers include instruction mnemonics,
    directive mnemonics, register designations, and other
    words that have a special meaning to the assembler.

## Program Format
    Assembler code is not case-sensitive, but it is good practice to
    • Use lowercase letters for instructions
    • Use uppercase letters for directives







# 3.2 32-Bit Example using Debugger

# Data Declarations

# Instruction Operands

# Complete 32-Bit Example Windows Input/Output

# Input/Output & Data Conversion Using Macros Defined in IO.H

# 64-Bit Examples

# Summary
