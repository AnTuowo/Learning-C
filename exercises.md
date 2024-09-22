# C, you are a Masochist
>You will die but C will live anyway
## Lecture 1
## Lecture 2
### Convert character to integer
- Method 1:
```c
#include <stdio.h>
#include <stdlib.h>

int convert(char var)
{
    return var - '0';  // Correct minus operator
}

int main()
{
    char variable = '5';
    int converted_value = convert(variable);  // This will convert '5' to 5
    printf("Converted value: %d\n", converted_value);  // Output the result
    return 0;
}
```
The output
```bash
Converted value: 5
```
- Method 2: "a" to i function (Atoi)
```c
int atoi(char s[], int size)
{
	num = 0;
	for (int i = 0; i < size; i++)
{
	num += 10 * num + convert(s[i]);
}
}

int main()
{
    int converted_value = atoi("12345", 5);
    return 0;
}

```