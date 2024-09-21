# (Not) Everything about C
>You will die but C will live

## Introduction
Created in 1972 by Dennis Ritchie at Bell Labs for the development of UNIX OS, C is a statically typed procedural language behind many of the tools which we are taking for granted today: MySQL, interpreter for Python, Git,...
## Features
```diff
+   C compiles directly to machine code with minimal runtime support. It gives developers low-level control over memory and hardware.
-   It is platform-dependent for specific OS (Mac, Linux or Windows only) and requires manual memory management.
```
## Create C file
 To start coding in C, you need to:
 1. install a compiler like GCC. 
 2. Create a .c file with a main function, where your program starts.
 3. Includes using library 
 4. The return value of the function indicates success (0) or failure (1).
## Types
- Int
- Char
- Float
- Double
- Short/Long
## Complex Data types
 C doesn't support OOP but allows custom data types with structures (structs). 
## Execute C file
```bash
gcc open.c -o open.exe
./open.exe
```
## Cya
