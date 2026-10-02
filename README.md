# Linux File System Simulator

This project is a console application written in C that simulates a Linux file system inside a virtual disk image. It is designed to model core filesystem behavior similar to an EXT2-style environment and allows users to interact with directories and files through command-line operations.

The program supports common file system actions such as:

- Listing directories (`ls`)
- Changing directories (`cd`)
- Printing the working directory (`pwd`)
- Creating directories and files (`mkdir`, `creat`)
- Removing entries (`rmdir`, `unlink`)
- Creating and resolving links (`link`, `symlink`, `readlink`)
- Opening, reading, writing, and closing files
- Copying files (`cp`)

This repository is intended for a Linux/Unix systems course or project environment and runs in a terminal-based shell on Ubuntu.

## Requirements

To build and run this project, you need:

- Ubuntu 20.04 or a compatible Linux environment
- GCC compiler installed
- A terminal shell
- Basic filesystem access permissions
- The repository files, including the generated disk image and build scripts

## Build and Run

The project includes a helper script to build and execute the simulator:

```bash
./mk
```

This script creates the virtual disk image and compiles the C source files before running the simulation.

If you want to build manually, use:

```bash
gcc main.c util.c -o a.out
./a.out mydisk
```

## Notes

- The simulator expects a virtual disk image such as `mydisk` or `disk2` to exist before execution.
- The project is meant to be run from the repository root in a Linux shell.
- The code is structured around a simplified filesystem implementation and is intended for educational and academic use.
