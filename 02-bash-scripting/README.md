# Bash Scripting Fundamentals

## What I Learned

Bash is a command-line shell commonly used on Linux systems. Bash scripting allows me to combine commands into a script so that tasks can be performed automatically.

## What Is a Shell Script?

A shell script is a text file containing commands that a shell executes in sequence.

A basic Bash script looks like this:

```bash
#!/bin/bash

echo "Hello, World!"
```

The first line identifies the interpreter used to execute the script. The `echo` command prints text to the terminal.

## Variables

Variables store values that can be reused.

Example:

```bash
#!/bin/bash

name="Student"
echo "Hello, $name"
```

In Bash, there must not be spaces around the `=` when assigning a variable.

## Command-Line Arguments

Arguments allow a script to receive input when it is run.

- `$0` — the script's name.
- `$1` — the first argument.
- `$2` — the second argument.
- `$#` — the number of arguments.
- `$@` — all positional arguments.

Example:

```bash
#!/bin/bash

echo "Script name: $0"
echo "First argument: $1"
```

If the script is run with `bash example.sh Linux`, the first argument is `Linux`.

## Conditions

The `if`, `elif`, and `else` statements allow a script to make decisions.

Example:

```bash
#!/bin/bash

if [ "$1" = "Linux" ]; then
    echo "Operating system topic selected."
else
    echo "Another topic selected."
fi
```

A condition is evaluated and the matching block is executed.

## Loops

Loops repeat commands.

Example:

```bash
#!/bin/bash

for item in one two three; do
    echo "$item"
done
```

This prints each item on a separate line.

## Running a Script

A script can be run using:

```bash
bash script.sh
```

Alternatively, make it executable and run it directly:

```bash
chmod +x script.sh
./script.sh
```

## Practice

I am learning to use variables, command-line arguments, conditions, loops, and basic input and output to create useful scripts.

## Cybersecurity Relevance

Bash scripting can help automate repetitive administrative tasks, process log files, check system settings, and support authorized security testing.

## Learning Source

pwn.college — hands-on Linux and shell scripting practice.

These notes explain general concepts in my own words and do not include restricted challenge solutions.
