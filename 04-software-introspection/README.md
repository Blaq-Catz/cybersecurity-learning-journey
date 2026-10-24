# Software Introspection

## Overview

Software introspection is the process of examining a program to understand how it works internally. In this section of my cybersecurity learning journey, I am learning how to inspect memory, debug running programs, understand command-line arguments, and observe program execution using GDB and other Linux tools.

## Topics Covered

### 1. Examining Memory with GDB

GDB allows us to inspect memory and display its contents in different formats.

Common commands:

```bash
x/d ADDRESS
x/a ADDRESS
x/s ADDRESS
```

- `x` — examines memory.
- `/d` — displays a value as a decimal number.
- `/a` — interprets a value as a memory address.
- `/s` — displays memory contents as a string.

These commands help us understand what data is stored in memory and how a program accesses it.

### 2. Understanding Pointers and Arguments

A pointer is a value that holds a memory address. It points to where data is stored rather than containing the data itself.

Important concepts:

- `argc` represents the number of command-line arguments, including the program name.
- `argv` contains pointers to the command-line argument strings.
- The initial process stack stores the argument count and pointers to the arguments.
- GDB can inspect a pointer and then examine the data at the address it references.

Understanding pointers is important for debugging, reverse engineering, and binary analysis.

### 3. Breakpoints and the `int3` Instruction

The x86 `int3` instruction generates a breakpoint exception. When a debugger such as GDB is attached, it can catch the exception and pause execution.

Example assembly:

```asm
.intel_syntax noprefix
.global _start

_start:
    mov rdi, 1337
    int3
```

In this example:

- `mov rdi, 1337` places the value `1337` in the `rdi` register.
- `int3` triggers a breakpoint exception.

Breakpoints allow us to inspect registers and program state at a specific point during execution.

### 4. Passing Command-Line Arguments in GDB

Programs often accept arguments when they are launched. GDB allows us to pass these arguments using `run`.

```gdb
run example
```

The shorter form is:

```gdb
r example
```

The argument is passed to the program in the same way as when launching it directly from the terminal.

This is useful when investigating programs that require particular command-line arguments.

### 5. Redirecting Standard Input

Standard input (`stdin`) is the stream through which a program receives input.

GDB supports input redirection when starting a program:

```gdb
run < /path/to/input
```

This sends the contents of a file to the program as standard input.

Input redirection is useful for testing programs with predefined input and reproducing specific behaviour during debugging.

## Important Commands

| Command | Description |
|---|---|
| `gdb ./program` | Opens a program in GDB |
| `starti` | Starts execution at the first instruction |
| `run` | Starts or restarts the program |
| `run example` | Runs a program with an argument |
| `stepi` | Executes one machine instruction |
| `info registers` | Displays processor registers |
| `disassemble` | Displays assembly instructions |
| `x/d ADDRESS` | Examines memory as a decimal value |
| `x/a ADDRESS` | Examines memory as an address |
| `x/s ADDRESS` | Examines memory as a string |
| `quit` | Exits GDB |

## Practical Skills Gained

By studying these topics, I am developing the ability to:

- Inspect memory using GDB.
- Understand pointers and how arguments are represented in memory.
- Observe processor registers during execution.
- Understand how software triggers breakpoints.
- Run programs with command-line arguments inside a debugger.
- Redirect file contents into a program's standard input.
- Investigate compiled programs more effectively.

## Why This Matters in Cybersecurity

Software introspection is an important foundation for:

- **Reverse engineering:** Understanding compiled programs.
- **Malware analysis:** Investigating suspicious software behaviour in a controlled environment.
- **Vulnerability research:** Examining memory and program execution.
- **Binary analysis:** Understanding machine instructions and processor registers.
- **Debugging:** Identifying errors and unexpected behaviour.

These concepts will support my continued learning in Linux, assembly, binary analysis, and ethical penetration testing.

## Learning Resources

- [pwn.college](https://pwn.college/)
- [GNU Debugger (GDB) Documentation](https://sourceware.org/gdb/documentation/)

---

*These notes document my learning and understanding of general software introspection concepts. They do not include challenge flags or challenge-specific solutions.*
