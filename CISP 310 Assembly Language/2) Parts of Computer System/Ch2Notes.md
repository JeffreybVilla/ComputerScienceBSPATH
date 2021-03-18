# x86 Registers General Purpose Registers
- The EAX, EDX, ECX, EBX, EBP, EDI, and ESI registers are 32-bit general-purpose registers, used for temporary data storage and memory access.

- The AX, DX, CX, BX, BP, DI, and SI registers are 16-bit equivalents of the above, they represent the low-order 16 bits of 32-bit registers.

- The AH, DH, CH, and BH registers represent the high-order 8 bits of the corresponding register

- Similarly, AL, DL, CL, and BL represent the low-order 8 bits of the registers.
![gp_registers (2)](https://user-images.githubusercontent.com/32498334/111692899-36200880-87ed-11eb-8353-afaa5d57368e.jpg)

















## General Registers: 32-Bit CPUs 
    Four 32-bit registers: EAX, EBX, ECX, EDX

    Four 16-bit registers: AX, BX, CX, DX

    Eight 8-bit registers: AH, AL, BH, BL, CH, CL, DH, DL 

## Some registers have special use
ECX for count in LOOP and repeatable instructions.

![32bit_registers](https://user-images.githubusercontent.com/32498334/111690750-d1fc4500-87ea-11eb-9f90-550d2ffc1ecf.png)


## Index Registers
- 2 index registers:
    - ESI (source index)
    - EDI (destination index)
- They both can be used as 16-bit or 32-bit registers
- Also in string processing instructions
- ESI & EDI can be used as general-purpose data registers.
![index_n_pointer_registers](https://user-images.githubusercontent.com/32498334/111691430-8b5b1a80-87eb-11eb-867a-78d82675e930.png)
