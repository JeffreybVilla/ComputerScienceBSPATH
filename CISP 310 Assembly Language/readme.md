# 0. Storage Units
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



# 1. Advantages of High-Level Languages
    - High-level language programs are portable.
        - (Although some programs could still have a few machine-dependent details, they can be used with little or no modifications on other types of machines.)

    - High-level instructions
        - Program development is faster
        - Fewer lines of code
        - Program maintenance is easier

    - Compiler translates to the target machine language.


# 2. Why program in Assembly?
    - There are some disadvantages...
        - Assembly language programs are not portable!
        - Learning the assembly is more difficult than learning Java!
        - Programming in the assembly language is a tedious and error-prone process.
        - High-level languages should be natural preference for common applications.

 
# 3. Here is why...
    - Assembly language programs contain only the code that is necessary to perform the given task.

    - Assembly gives direct and complete control over system hardware:
        - Writing device drivers.
        - Operating system design.
        - Embedded systems programming, e.g. aviation industry.
        - Writing in-line assembly (mixed-mode) in high-level languages such as C/C++, or hybrid programming in assembly and C/C++.


# 4. Speed, Efficiency, Debugging, Optimization...
    - There are areas where speed is everything, for example, internet data encryption, aircraft navigational systems, medical hardware control...

    - There are also areas where space-efficiency is everything: spacecraft control software...

    - Understanding disassembly view of an executable program is also useful:
        - for investigating the cause of a serious bugs or crashes that require understanding of memory dumps and disassembled code.
        - for optimizing your code.
        - for practical and educational purposes.






# 11. Runtime Environment
    - Program runs on the processor.

    - Program uses operating system functions and services.

    - Program uses one of the memory models:
        - Real mode flat model, 65,536 bytes of addressable memory (ancient MS-DOS .COM files)
        - Real mode segmented model, 1 megabyte (prime-time MS-DOS)
        - Protected mode flat model, modern Windows and Linux:
            - Addressable Memory: 80486 and Pentium - 4 Gigabytes
            - As far as 32-bit Vista is concerned, the world ends at 4,096 megabytes.
            - A 32-bit program can address up to 4 gigabytes of memory.

## Example
    ; CIS-77
    ; your_program_name.asm
    ; Brief description of what the program does

    .386                ; Tells MASM to use Intel 80386 instruction set.
    .MODEL FLAT         ; Flat memory model
    option casemap:none ; Treat labels as case-sensitive

    .CONST              ; Constant data segment

    .STACK 100h         ; (default is 1-kilobyte stack)

    .DATA               ; Begin initialized data segment

    .CODE               ; Begin code segment
    _main PROC          ; Beginning of code

        ret

    _main ENDP
    END _main           ; Marks the end of the module and sets the program entry point label



# 12. Assembly & C-Code Compared
    - Some simple high-level language instructions can be expressed by a single assembly instruction:

    Assembly Code           C Language Code
    ----------------        ---------------------------------
    inc result              ++result;    // Increment value
    mov size,  1024         size = 1024; // Assign value
    and var,   128          var &= 128;  // Apply AND bitmask
    add value, 10           value += 10; // Addition

# 13. More Assembly & C -Code
    - Most high-level language instructions need more than one assembly instruction:

    Assembly Code           C Language Code
    ----------------        ---------------------------------
    mov AX,   value         size = value;     // Assign variable
    mov size, AX

    mov AX,   sum           sum += x + y + z; // Arithmetic computation
    add AX,   x
    add AX,   y
    add AX,   z
    mov sum,  AX



# 14. Assembly vs. Machine Language
    - Assembly Language uses mnemonics, digital numbers, comments, etc.

    - Machine Language instructions are just a sequences of 1s and 0s.

    - Readability of assembly language instructions is much better than the machine language instructions:

    Assembly Language   Machine Language (in Hex)
    -----------------   --------------------------
    inc result          FF060A00
    mov size,  45       C7060C002D00
    and var,   128      80260E0080
    add value, 10       83060F000A




# 15. Controlling Program Flow
    - Just as in high-level language, you want to control program flow.

    - The JMP instruction transfers control unconditionally to another instruction.

    - JMP corresponds to goto statements in high-level languages:

    ; Handle one case
    label1: .
            .
            .
            jmp done

    ; Handle second case
    label2: .
            .
            .
            jmp done
            .
            .
    done:



# 16. Conditional Jumps
    - Conditional jump is taken only if the condition is met.

    - Condition testing is separated from branching.

    - Flag register is used to convey the condition test result.

    For example:

            cmp    ax, bx
            je     done
            .
            .
    done:





# 17. General Purpose Registers
    - The EAX, EDX, ECX, EBX, EBP, EDI, and ESI registers are 32-bit general-purpose registers, used for temporary data storage and memory access.

    - The AX, DX, CX, BX, BP, DI, and SI registers are 16-bit equivalents of the above, they represent the low-order 16 bits of 32-bit registers.

    - The AH, DH, CH, and BH registers represent the high-order 8 bits of the corresponding register

    - Similarly, AL, DL, CL, and BL represent the low-order 8 bits of the registers.
![gp_registers (2)](https://user-images.githubusercontent.com/32498334/111692899-36200880-87ed-11eb-8353-afaa5d57368e.jpg)


# 18. Typical Uses of General-Purpose Registers
![TypicalRegisters](https://user-images.githubusercontent.com/32498334/111693199-90b96480-87ed-11eb-8548-43089d721956.png)


# 19. x86 Registers
    - Four 32-bit registers can be used as
        - Four 32-bit registers: EAX, EBX, ECX, EDX

        - Four 16-bit registers: AX, BX, CX, DX

        - Eight 8-bit registers: AH, AL, BH, BL, CH, CL, DH, DL 

    - Some registers have special use
        - ECX for count in LOOP and repeatable instructions.

![32bit_registers](https://user-images.githubusercontent.com/32498334/111690750-d1fc4500-87ea-11eb-9f90-550d2ffc1ecf.png)


# 20. x86 Index Registers & Pointer Registers
    - 2 index registers:
        - ESI (source index)
        - EDI (destination index)

        - They both can be used as 16-bit or 32-bit registers
        - Also in string processing instructions
        - ESI & EDI can be used as general-purpose data registers.

    - 2 Pointer registers:
        - ESP (Stack pointer)
        - EBP (Base pointer)

        - 16-bit or 32-bit registers
        - Used exclusively to maintain the stack.
![index_n_pointer_registers](https://user-images.githubusercontent.com/32498334/111691430-8b5b1a80-87eb-11eb-867a-78d82675e930.png)







# 21. x86 Control Registers
    - EIP 32-bit: 
        - Holds address of next instruction to be fetched for execution.

    - EFLAGS 32-bit: 
        - Collection of flags, or status bits.
        - Records information about many operations
        - Status flags: records status info about result of the last arithmetic/logical instruciton.
        - Direction flag: stores forward/backward direction for data copying.
        - System flags:
            - IF interrupt-enable mode
            - TF Trap flag used in single-step debugging.
        - Carry flag (CF) is bit 0
        - Zero flag (ZF) is bit 6
        - Sign flag (SF) is bit 7
        - Overflow flag (OF) is bit 11

# EXAMPLE: How flags are set by instructions
    - Consider this instruction: ADD EAX, 158
        - This instruction affects CF, OF, PF, SF, and ZF.
        - Suppose that EAX contains the word FF FF FF F3 prior to execution of the instruction.
        - Since 158 = the doubleword 00 00 00 9E
        - This instruction adds FF FF FF F3 and 00 00 00 9E
        - Putting the sum 00 00 00 91 in the EAX register.
        - It sets the carry flag CF to 1 since there is a carry.
        - The overflow flag OF is set to 0 since there is no overflow.
        - The sign flag SF is set to 0 (The leftmost bit of the sum 00 00 00 91)
        - Zero flag ZF is set to 0 since the sum is not 0.
