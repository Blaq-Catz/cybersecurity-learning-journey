# Linux Fundamentals

## What I Learned

Linux is an operating system widely used in servers, cloud computing, software development, and cybersecurity. The command line allows users to interact with the operating system by entering commands in a terminal.

## Basic Linux Commands

| Command | Purpose |
|---|---|
| `pwd` | Displays the current working directory. |
| `ls` | Lists files and directories. |
| `cd` | Changes the current directory. |
| `mkdir` | Creates a directory. |
| `touch` | Creates an empty file. |
| `cat` | Displays file contents. |
| `cp` | Copies files or directories. |
| `mv` | Moves or renames files. |
| `rm` | Removes files. |
| `whoami` | Displays the current username. |
| `clear` | Clears the terminal screen. |

## Files and Directories

Linux organizes files and directories in a hierarchical structure that starts at the root directory, `/`.

Important paths include:

- `/home` — contains users' home directories.
- `/etc` — contains system configuration files.
- `/tmp` — stores temporary files.
- `/var` — contains variable data, including many system logs.
- `/root` — the root user's home directory.

## Permissions and Users

Linux permissions control who can read, write, or execute a file.

- `r` — read permission.
- `w` — write permission.
- `x` — execute permission.

The command `ls -l` displays file permissions and ownership.

The `chmod` command changes permissions, while `chown` changes file ownership. Administrative commands should be used carefully.

## Processes

A process is a running instance of a program.

Useful commands include:

- `ps` — displays information about processes.
- `top` — provides a live view of processes and resource usage.
- `kill` — sends a signal to a process.
- `jobs` — lists jobs started in the current shell.

## Practice

I am practising navigating directories, creating files, reading file contents, understanding permissions, and inspecting running processes.

## Cybersecurity Relevance

Linux knowledge helps me understand system administration, investigate suspicious activity, manage access permissions, and work with security tools.

## Learning Source

pwn.college — hands-on Linux and cybersecurity learning.

These notes summarize concepts in my own words and do not contain restricted challenge solutions.
