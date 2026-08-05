# Experiment: Design DFA to Accept the Strings "a", "ac", and "bac"

## Aim

To design a Deterministic Finite Automaton (DFA) using a simulator that accepts only the input strings **"a"**, **"ac"**, and **"bac"**.

---

## Algorithm

1. Start the DFA from the initial state.
2. If the first input symbol is **`a`**, move to the next state.
3. If the input ends after **`a`**, accept the string.
4. If the next symbol after **`a`** is **`c`**, move to the accepting state and accept **`ac`**.
5. If the first symbol is **`b`**, move to another state.
6. From that state, read **`a`** and move to the next state.
7. Read **`c`** and move to the accepting state to accept **`bac`**.
8. For any invalid input or transition, move to a dead state.
9. Stop the DFA.

---

## Sample Input and Output

### Sample Input 1

```text
a
```

### Sample Output 1

```text
Accepted
```

---

### Sample Input 2

```text
ac
```

### Sample Output 2

```text
Accepted
```

---

### Sample Input 3

```text
bac
```

### Sample Output 3

```text
Accepted
```

---

### Sample Input 4

```text
abc
```

### Sample Output 4

```text
Rejected
```

---

### Sample Input 5

```text
bacb
```

### Sample Output 5

```text
Rejected
```

---

## Result

Thus, the DFA was successfully designed using the simulator to accept only the strings **"a"**, **"ac"**, and **"bac"**, and reject all other input strings.
