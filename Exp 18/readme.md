# Design DFA to Accept Even Number of a's

## Aim
To design and simulate a Deterministic Finite Automaton (DFA) that accepts all strings containing an **even number of a's** over the alphabet **{a, b}**.

---

## Algorithm

### Step 1:
Start the DFA from the initial state **q0**, which represents an even number of **a's** (including zero).

### Step 2:
Read the input string one symbol at a time.

### Step 3:
If the input symbol is **a** while in **q0**, move to **q1** (odd number of **a's**).

### Step 4:
If the input symbol is **a** while in **q1**, move back to **q0** (even number of **a's**).

### Step 5:
If the input symbol is **b**, remain in the current state since **b** does not affect the count of **a's**.

### Step 6:
Repeat the process until all input symbols are processed.

### Step 7:
If the DFA ends in **q0**, accept the string; otherwise, reject it.

---

## Accepted Strings
- ε (empty string)
- bb
- aa
- abab
- baab
- aabbaa

## Rejected Strings
- a
- ab
- baa
- aaa
- baba
