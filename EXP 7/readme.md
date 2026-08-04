# Experiment: Check Whether a String Belongs to the Context Free Grammar

## Aim

To write a C program to check whether a given binary string belongs to the Context Free Grammar (CFG):

**S → 0S1 | ε**

---

## Algorithm

1. Start the program.
2. Read the input binary string.
3. Find the length of the string.
4. Check whether the string contains only `0` and `1`.
5. Initialize two pointers:
   - `i` at the beginning of the string.
   - `j` at the end of the string.
6. Compare the characters:
   - The left character must be `0`.
   - The right character must be `1`.
7. Move the pointers inward until they meet or cross.
8. If all pairs satisfy the condition and no extra characters remain, the string belongs to the grammar.
9. Otherwise, the string does not belong to the grammar.
10. Display the result.
11. Stop the program.

---

## Program

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char str[100];
    int i, j, len, flag = 1;

    printf("Enter a binary string: ");
    scanf("%s", str);

    len = strlen(str);

    // Check whether the string contains only 0 and 1
    for(i = 0; i < len; i++)
    {
        if(str[i] != '0' && str[i] != '1')
        {
            flag = 0;
            break;
        }
    }

    if(flag)
    {
        i = 0;
        j = len - 1;

        while(i < j)
        {
            if(str[i] == '0' && str[j] == '1')
            {
                i++;
                j--;
            }
            else
            {
                flag = 0;
                break;
            }
        }

        // If one unmatched character remains, reject
        if(i == j)
            flag = 0;
    }

    if(flag)
        printf("The string belongs to the grammar.\n");
    else
        printf("The string does not belong to the grammar.\n");

    return 0;
}
```

---

## Sample Input and Output

### Sample Input 1

```text
Enter a binary string: 0011
```

### Output

```text
The string belongs to the grammar.
```

---

### Sample Input 2

```text
Enter a binary string: 000111
```

### Output

```text
The string belongs to the grammar.
```

---

### Sample Input 3

```text
Enter a binary string: 01
```

### Output

```text
The string belongs to the grammar.
```

---

### Sample Input 4

```text
Enter a binary string: 0101
```

### Output

```text
The string does not belong to the grammar.
```

---

### Sample Input 5

```text
Enter a binary string: 00111
```

### Output

```text
The string does not belong to the grammar.
```

---

## Result

Thus, the C program to check whether a given binary string belongs to the Context Free Grammar **S → 0S1 | ε** was successfully implemented and executed. The program correctly accepts strings of the form **0ⁿ1ⁿ** (including the empty string) and rejects all other strings.
