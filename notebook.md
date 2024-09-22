# (Not) Everything about C
>You will die but C will live

## Introduction
Created in 1972 by Dennis Ritchie at Bell Labs for the development of UNIX OS, C is a statically typed procedural language behind many of the tools which we are taking for granted today: MySQL, interpreter for Python, Git,...
## Features
```diff
+   C compiles directly to machine code with minimal runtime support.
+   It gives developers low-level control over memory and hardware.
-   It is platform-dependent for specific OS (Mac, Linux or Windows only). 
-   It requires manual memory management.
```
## Create C file
 To start coding in C, you need to:
 1. install a compiler like GCC. 
 2. Create a .c file with a main function, where your program starts.
 3. Includes using libraries 
 4. The return value of the function indicates success (0) or failure (1).
 ```c
#include <stdio.h>

int main()
{
    printf("Hello World");

    return 0;
}
 ```
## Types

| Type | Definition |
| ----------- | ----------- |
| Int | Integer |
| Float |  Floating point number |
| Char | Character |
| Short | Short integer |
| Long | Long ineger |
| Double | Double-precision floating point |
### How to use?
```c
#include <stdio.h>

int main()
{
    // type name = value;
    int birthday = 1107;

    // Print out the output
    printf("Value: %i \n", birthday);

    //Print out the adresse using &    
    printf("Adresse: %p \n", &birthday);    

    return 0;
}
```
The output should look like this:
```bash
Value: 1107 
Adresse: 0x7ffebaa83384 
```
### String
There is **NO** string type. We use *char* instead which represents a one by character stored as an integer.

1.  A string can be created with **an array of characters**. Each letter will have its own memory and be ended by a null character.
```c
#include <stdio.h>

int main() {
    char str[] = "Hey";  
    for (int i = 0; i <= 3; i++) {
        printf("Char: '%c'. ", str[i]);      
        printf("Address: %p \n", &str[i]);  
    }

    return 0;
}
```
Ouput:
```bash
Char: 'H'. Address: 0x7fff499b66c4 
Char: 'e'. Address: 0x7fff499b66c5 
Char: 'y'. Address: 0x7fff499b66c6 
Char: ''. Address: 0x7fff499b66c7  
```

2. Starting with a pointer, we allocate memory space for it by using * and malloc.
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    // Allocate 4 bytes of memory
    char *str = malloc(4);

    // Assign values 
    str[0] = 'H';
    str[1] = 'e';
    str[2] = 'y';
    str[3] = '\0';

    // all done now so free memory to avoid memory leaks
    free(str);

    return 0;
}
```

## Complex Data Types
 C doesn't support OOP but allows custom data types with structures (structs). 
 ```c
 #include <stdio.h>

//Create a struct
struct Person {
    char name[50];
    int age;
    float height;
};

int main() {
    struct Person goat = {"Messi", 37, 1.70};  
    printf("Name: %s\nAge: %d\nHeight: %.2f meters\n", goat.name, goat.age, goat.height);
    return 0;
}

 ```
 The ouput
 ```bash
Name: Messi
Age: 37
Height: 1.70 meters

 ```
## Execute C file
```bash
gcc open.c -o open.exe
./open.exe
```

## Control structures
### Branching
- If-Else
```c
if (<expression>) { // full then/else form
<statement>
}
else {
<statement>
}
```
- Switch (pls use with caution!)
```c
<switch (<expression>) {
    case <const-expression-1>:<statement>
    break;

    case <const-expression-2>:<statement>
    break;

    // optional
    default: // optional
<statement>
}

```
- **Conditional Expression**
```c
//Instead of this
//  if (x < y) {
//      min = x;
//  }
//  else {
//      min = y;
//  }
// Use this

min = (x < y) ? x : y;
```
### Loop
- For
```c
for (i = 0; i < 10; i++) {
<statement>
}
```
- While
```c
while (<expression>) {
<statement>
}
```
- Do-While
```c
do {
<statement>
} while (<expression>)
```
- Break (pls use with caution)
```c
while (<expression>) {
<statement>
<statement>
if (<condition which can only be evaluated here>)
break;
<statement>
<statement>
}
//Control jumps here when break triggered
```

- Continue (pls use with caution)
```c
while (<expression>) {
...
if (<condition>)
continue;
...
...
// control jumps here on the continue
}
```

### Stack vs Heap
## Cya
