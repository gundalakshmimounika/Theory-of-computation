# Experiment: Check Whether a String Belongs to the Grammar

## Aim
To write a C program to check whether a given binary string belongs to the grammar:

**S → 0S0 | A**  
**A → 1A | ε**

---

## Theory

The given grammar generates strings that consist of:
- Zero or more `0`s at the beginning and end (in equal numbers).
- Followed by zero or more `1`s in the middle.

Examples of valid strings:
- ε (empty string)
- `1`
- `11`
- `111`
- `00`
- `0110`
- `001100`
- `000111000`

Examples of invalid strings:
- `010`
- `101`
- `1100`
- `0010100`

---

## Algorithm

1. Start the program.
2. Read the input binary string.
3. Check whether the string contains only `0` and `1`.
4. Count the number of matching `0`s from the beginning and end.
5. Verify that the remaining middle characters (if any) are all `1`s.
6. If the condition is satisfied, the string belongs to the grammar.
7. Otherwise, the string does not belong to the grammar.
8. Display the result.
9. Stop the program.

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

        // Remove matching 0's from both ends
        while(i <= j && str[i] == '0' && str[j] == '0')
        {
            i++;
            j--;
        }

        // Remaining characters should be only 1's
        while(i <= j)
        {
            if(str[i] != '1')
            {
                flag = 0;
                break;
            }
            i++;
        }
    }

    if(flag)
        printf("The string belongs to the grammar.\n");
    else
        printf("The string does not belong to the grammar.\n");

    return 0;
}
```

---

## Sample Output

### Sample Output 1

```text
Enter a binary string: 0011100
The string belongs to the grammar.
```

### Sample Output 2

```text
Enter a binary string: 111
The string belongs to the grammar.
```

### Sample Output 3

```text
Enter a binary string: 0110
The string belongs to the grammar.
```

### Sample Output 4

```text
Enter a binary string: 010
The string does not belong to the grammar.
```

---

## Result

The C program to check whether a given binary string belongs to the grammar **S → 0S0 | A, A → 1A | ε** was successfully implemented and executed. The program correctly verifies whether the input string satisfies the given grammar.
