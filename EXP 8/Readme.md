# Experiment: Check Whether a String Belongs to the Context Free Grammar (CFG)

## Aim

To write a C program to check whether a given binary string belongs to the language defined by the Context Free Grammar (CFG):

**S → A101A**  
**A → 0A | 1A | ε**

---

## Algorithm

1. Start the program.
2. Read the input binary string.
3. Check whether the string contains only binary digits (`0` and `1`).
4. Search for the substring **"101"** in the given string.
5. If the substring **"101"** is present, the string belongs to the given grammar because `A` can generate any sequence of `0`s and `1`s (including the empty string).
6. If the substring **"101"** is not present, the string does not belong to the grammar.
7. Display the appropriate result.
8. Stop the program.

---

## Sample Input and Output

### Sample Input 1

```text
Enter a binary string: 101
```

### Sample Output 1

```text
The string belongs to the grammar.
```

---

### Sample Input 2

```text
Enter a binary string: 001011
```

### Sample Output 2

```text
The string belongs to the grammar.
```

---

### Sample Input 3

```text
Enter a binary string: 11010100
```

### Sample Output 3

```text
The string belongs to the grammar.
```

---

### Sample Input 4

```text
Enter a binary string: 111000
```

### Sample Output 4

```text
The string does not belong to the grammar.
```

---

## Result

Thus, the C program to check whether a given binary string belongs to the Context Free Grammar **S → A101A, A → 0A | 1A | ε** was successfully implemented and verified using sample test cases.
