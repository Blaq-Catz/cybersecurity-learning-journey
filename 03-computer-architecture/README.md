# Computer Architecture and Assembly Fundamentals

## What I Learned

Computer architecture explains how a computer's processor, memory, registers, and other components work together to execute instructions.

Understanding these concepts helps me learn how programs interact with the operating system and how software operates at a lower level.

## The CPU

The Central Processing Unit (CPU) executes program instructions.

Its main responsibilities include:

- Performing arithmetic and logical operations.
- Processing instructions.
- Moving data between registers and memory.
- Coordinating program execution.

## Registers

Registers are small, fast storage locations inside the CPU.

On x86-64 systems, examples include:

- `rax` — commonly used for arithmetic and function results; also used for system call numbers in the Linux system call convention.
- `rbx` — a general-purpose register.
- `rcx` — a general-purpose register with several instruction-specific uses.
- `rdx` — a general-purpose register often used for data and arguments.
- `rsp` — points to the top of the stack.
- `rbp` — often used as a frame pointer, although compilers may use it for other purposes.
- `rip` — identifies the instruction being executed next.

## Memory and the Stack

Programs use memory to store instructions and data.

Important concepts include:

- **Stack:** commonly stores function call information and local data.
- **Heap:** commonly used for dynamically allocated memory.
- **Code or text segment:** contains program instructions.
- **Data segment:** stores certain global and static variables.

The exact memory layout depends on the program and operating system.

## Machine Code and Assembly

Machine code consists of instructions encoded as bytes that a processor can execute.

Assembly language represents processor instructions in a more human-readable form.

For example, an x86-64 instruction might look like this:

```asm
mov rax, 60
```

This places the value `60` into the `rax` register. The meaning of an instruction depends on the processor architecture and instruction set.

## System Calls

A system call allows a program to request a service from the operating system kernel.

Examples include requesting file operations, creating processes, and writing output.

On Linux x86-64, the `syscall` instruction is used to enter the kernel through the system call interface.

## Assembling and Linking

An assembly source file must generally be assembled into an object file. A linker can then combine object files and libraries to produce an executable.

Common tools include:

- `as` — GNU assembler.
- `ld` — GNU linker.
- `objdump` — displays information about object files and machine instructions.

## Practice

I am learning how instructions, registers, memory, assembly, and system calls fit together.

## Cybersecurity Relevance

Computer architecture helps me understand program execution, debugging, memory-related vulnerabilities, reverse engineering, and how software interacts with the operating system.

## Learning Source

pwn.college — hands-on computer systems and assembly learning.

These notes describe general concepts in my own words and do not include restricted challenge solutions.
