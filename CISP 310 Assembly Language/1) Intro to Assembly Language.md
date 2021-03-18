# What is assembly language and its importance?
    - Processor-Dependent
    - Low-Level Programming Language
    - Assembly code is converted into executable machine code by a utility program refereed to as an assembler.


    - Each family of CPUs has its own set of instructions or its own Assembly Language for handling various operations.
      - Getting input from keyboard
      - Displaying information on screen
      - Performing various tasks


    - There are many different types of Assembly Languages for different types of CPU Architectures.
    - Popular Architectures today:
      - ARM: Phones
      - MIPS: Video Game Consoles
      - x86: Intel PCs and others 16-bit to 64-bit


    - Set of instructions written in assembly language are called "machine language instructions"
    - Our processors (CPU) only understands machine language instructions which are stringsn of 1's & 0's.
    - Assembly code is converted into executable machine code by a utlitiy program referred to as an assembler. 


## Why Assembly?
    - Directly communicate with hardware using human readable text.
    - Direct hardware manipulation.
    - Access to specialized processor instructions.
    - Writing device drivers
    - Operating system design.
    - Embeded system program, etc.


## Will help you understand
    - How data is represented in memory and other external devices. 
    - How programs interface with your operating system, processor, and BIOS. 
    - How the processor accesses and executes instructions.
    - How instructions access and process data.
    - How a program accesses external devices. 





# Basics of Computer Hardware
## Main internal hardware
    - Processor:
    - Memory:
    - Registers: Are processor components that hold data and addresses.

    In order to execute a program the system copies this into an internal memory and then the processor executes the program instructions.


# Storage Units
    Computer storage unit is called a bit.
    A bit can be 0 (OFF) or 1 (ON).
    8 bits = 1 byte.
    2 byte = Word.

    Word: 2-byte data item
    Doubleword: 4-byte (32-bit) data item
    Quadword: 8-byte (64-bit) data item
    Paragraph: 16-byte (128 bit) area
    Kilobyte: 1024 bytes
    Megabytes: 1,048,576 bytes


# Number System
- Decimal Number System:      base 10
- Binary Number System:       base 2
- Hexadecimal Number System:  base 16
- Octal Number System:        Base 8


## Denary/Decimal Number System
- Base 10
- Standard system for denoting integer and non-integer numbers.
- Uses digits to represent all the numbers.
EX: 1, 2, 3, ...


## Binary Number System
- Base 2
- Begins at 0 and increase by 1
- The value of a binary number is based on the presence of 1 bit and their positional value.
EX: 1 = 0001


## Hexadecimal Number System 
- Base 16 
- Digits range from 0 to 15
- Letters A through F represent 10 through 15
- Used for abbreviating lengthy binary
- To convert hexadecimal to binary, break it into groups of 4 consecutive groups each and write corresponding digits.
    EX: 0001 1101 = 1D
- To convert hexadecimal to binary, write each hexadecimal digit into its 4-digit binary equivalent.
    EX: 2E = 0010 1110
    

## Octal Number System
- Base 8
- Uses digits 0 to 7
- Can be made from binary numbers by grouping consecutive binary digits into groups of three
    EX: decimal 12 = 014 in octal






# Execution Cycle
- The process through which the processor controls the execution of instructions.
1. Fetch
2. Decode
3. Execute





# Start writing your first assembly program x86
        1. Need an IDE for Assembly Language
        2. Need Official x86 Assembly Language Reference Manual
        3. Program Stucture


         .586
        .MODEL FLAT
        .STACK 4096
        INCLUDE io.h ;header file for input/output
        
        .DATA
        sum DWORD ?

        .CODE
        _MainProc PROC
                mov eax, 7
                add eax, 4
                mov sum, eax

                mov     eax, 0 ;exit with return code 0
                ret
        _MainProc ENDP
        END







# Understanding Registers
- One of the main tools to write programs in x86 assembly are the processor registers.
- You can, informally, think of registers as variables that are built in the processor.
- Using registers instead of memory to store values, makes the process faster and more efficient. 
- Instructions are executed sequentially
- x86 CPU has eight 32-bit General-Purpose Registers
    - eax, ecx, edx, ebx, esp, ebp, esi, edi
    - These registers are used for temporary data storage and memory access. 
