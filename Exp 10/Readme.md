# Experiment: Design a Push Down Automata (PDA)

## Aim

To design a Push Down Automata (PDA) that accepts the language consisting of all strings over the alphabet `{a, b}` in which the number of **a's is even**.

---

## Algorithm

1. Start the PDA from the initial state.
2. Read the input string one symbol at a time.
3. Count the occurrence of symbol `a` by changing states:
   - On reading an `a`, move between the even and odd states.
   - On reading a `b`, remain in the current state.
4. After reading the complete string:
   - If the number of `a`s is even, accept the string.
   - Otherwise, reject the string.
5. Stop.

---

## Sample Input and Output

### Sample Input 1

```text
abba
```

### Sample Output 1

```text
Accepted
```

---

### Sample Input 2

```text
bbbb
```

### Sample Output 2

```text
Accepted
```

---

### Sample Input 3

```text
aaab
```

### Sample Output 3

```text
Rejected
```

---

### Sample Input 4

```text
aabb
```

### Sample Output 4

```text
Accepted
```

---

## Result

Thus, the Push Down Automata (PDA) was successfully designed to accept all strings over the alphabet `{a, b}` having an even number of `a`s.
