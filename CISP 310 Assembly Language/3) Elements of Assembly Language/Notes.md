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
## Framework Packages
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20310%20Assembly%20Language/images/frameworks.png)

## Debugger Memory Display
    Shows the starting memory address for each line.

    Shows the 2 hex digits for each byte memory byte
        • If the byte can be interpreted as a printable ASCII character, that character is
        displayed to the right.
        • Otherwise, a period is displayed to the right.

## Output of Assembler
    Object file (e.g., example.obj)
        • Contains machine language statements almost ready to execute

    Listing file (e.g., example.lst)
        • Shows how the assembler translated the source program

## Listing File
    00000000 .DATA
    00000000 FFFFFF97 number DWORD -105
    00000004 00000000 sum DWORD ?
    00000000 .CODE
    00000000 main PROC
    00000000 A1 00000000 R mov eax, number
    00000005 05 0000009E add eax, 158
    0000000A A3 00000004 R mov sum, eax















# 3.3 Data Declarations
This section explains the formats of operands used in BYTE, WORD, DWORD, and QWORD directives.
![](https://github.com/JeffreybVilla/ComputerScienceBSPATH/blob/main/CISP%20310%20Assembly%20Language/images/dataDeclarations.png)

## BYTE Directive
Examples:
byte1   BYTE 255            ; value is FF
byte2   BYTE 91             ; value is 5B
byte3   BYTE 0              ; value is 00
byte4   BYTE -1             ; value is FF
byte5   BYTE 6 DUP (?)      ; 6 bytes each with 00
byte6   BYTE 'm'            ; value is 6D
byte7   BYTE "Joe"          ; 3 bytes with 4A 6F 65

## DWORD Directive
Reserves storage for one or more doublewords of data, optionally initializing storage

Examples:
double1     DWORD -1                ; value is FFFFFFFF
double2     DWORD -1000             ; value is FFFFFC18
double3     DWORD -2147483648       ; value is 80000000
double4     DWORD 0, 1              ; two doublewords
Double5     DWORD 100 DUP (?)       ; 100 doublewords

## Multiple Operands
Separated by commas
• DWORD 10, 20, 30      ; three doublewords

Using DUP
• DWORD 100 DUP (?)     ; 100 doublewords

Character strings (BYTE directive only)
• BYTE "ABCD"           ; 4 bytes

## Parts of an Instruction
Instruction’s object code begins with the opcode, usually one byte
    • mov eax, number

Instruction operand
    • add eax, 158

## Types of Instruction Operands
Immediate mode
• Constant assembled into the instruction

Register mode
• A code for a register is assembled into the instruction

Memory references
• Several different modes












# Instruction Operands

# Complete 32-Bit Example Windows Input/Output

# Input/Output & Data Conversion Using Macros Defined in IO.H

# 64-Bit Examples

# Summary
