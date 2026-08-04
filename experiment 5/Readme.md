# Experiment: Check Whether a String Belongs to the Grammar

## Aim
To write a C program to check whether a given binary string belongs to the grammar:

**S → 0S0 | 1S1 | 0 | 1 | ε**

---

## Algorithm

1. Start the program.
2. Read the input binary string.
3. Find the length of the string.
4. Check whether the string contains only `0` and `1`.
5. Compare the first and last characters, second and second-last characters, and so on.
6. If all corresponding characters are equal, the string is a palindrome and belongs to the grammar.
7. Otherwise, the string does not belong to the grammar.
8. Display the result.
9. Stop the program.



## Sample Output

### Sample Output 1

```text
Enter a binary string: 1001
The string belongs to the grammar.
```

### Sample Output 2

```text
Enter a binary string: 0110
The string belongs to the grammar.
```

### Sample Output 3

```text
Enter a binary string: 0101
The string does not belong to the grammar.
```

---

## Result

The C program to check whether a given binary string belongs to the grammar **S → 0S0 | 1S1 | 0 | 1 | ε** was successfully implemented and executed. The program correctly identifies whether the input string belongs to the given grammar by verifying that it is a binary palindrome.
