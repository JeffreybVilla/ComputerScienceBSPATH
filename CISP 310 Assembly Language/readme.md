# 1. Advantages of High-Level Languages
### High-level language programs are portable.
    (Although some programs could still have a few machine-dependent details, they can be used with little or no modifications on other types of machines.)

### High-level instructions

    - Program development is faster

    - Fewer lines of code

    - Program maintenance is easier

### Compiler translates to the target machine language.

# 17. General Purpose Registers
- The EAX, EDX, ECX, EBX, EBP, EDI, and ESI registers are 32-bit general-purpose registers, used for temporary data storage and memory access.

- The AX, DX, CX, BX, BP, DI, and SI registers are 16-bit equivalents of the above, they represent the low-order 16 bits of 32-bit registers.

- The AH, DH, CH, and BH registers represent the high-order 8 bits of the corresponding register

- Similarly, AL, DL, CL, and BL represent the low-order 8 bits of the registers.
![gp_registers (2)](https://user-images.githubusercontent.com/32498334/111692899-36200880-87ed-11eb-8353-afaa5d57368e.jpg)


# 18. Typical Uses of General-Purpose Registers
![TypicalRegisters](https://user-images.githubusercontent.com/32498334/111693199-90b96480-87ed-11eb-8548-43089d721956.png)


# 19. x86 Registers
### Four 32-bit registers can be used as
    Four 32-bit registers: EAX, EBX, ECX, EDX

    Four 16-bit registers: AX, BX, CX, DX

    Eight 8-bit registers: AH, AL, BH, BL, CH, CL, DH, DL 

### Some registers have special use
    ECX for count in LOOP and repeatable instructions.

![32bit_registers](https://user-images.githubusercontent.com/32498334/111690750-d1fc4500-87ea-11eb-9f90-550d2ffc1ecf.png)


# 20. x86 Index Registers & Pointer Registers
### 2 index registers:
    - ESI (source index)
    - EDI (destination index)
    
    - They both can be used as 16-bit or 32-bit registers
    - Also in string processing instructions
    - ESI & EDI can be used as general-purpose data registers.

### 2 Pointer registers:
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
### Consider this instruction: ADD EAX, 158
- This instruction affects CF, OF, PF, SF, and ZF.
- Suppose that EAX contains the word FF FF FF F3 prior to execution of the instruction.
- Since 158 = the doubleword 00 00 00 9E
- This instruction adds FF FF FF F3 and 00 00 00 9E
- Putting the sum 00 00 00 91 in the EAX register.
- It sets the carry flag CF to 1 since there is a carry.
- The overflow flag OF is set to 0 since there is no overflow.
- The sign flag SF is set to 0 (The leftmost bit of the sum 00 00 00 91)
- Zero flag ZF is set to 0 since the sum is not 0.
