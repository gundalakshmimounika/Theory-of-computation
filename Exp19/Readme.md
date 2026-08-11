# Design DFA to Accept Odd Number of a's

## Aim
To design and simulate a Deterministic Finite Automaton (DFA) that accepts all strings containing an **odd number of a's** over the alphabet **{a, b}**.

---

## Algorithm

### Step 1:
Start the DFA from the initial state **q0**, which represents an even number of **a's** (initially zero).

### Step 2:
Read the input string one symbol at a time.

### Step 3:
If the input symbol is **a** while in **q0**, move to **q1** (odd number of **a's**).

### Step 4:
If the input symbol is **a** while in **q1**, move back to **q0** (even number of **a's**).

### Step 5:
If the input symbol is **b**, remain in the current state since **b** does not change the count of **a's**.

### Step 6:
Continue reading the input until all symbols are processed.

### Step 7:
If the DFA ends in **q1**, accept the string; otherwise, reject it.

---

## Accepted Strings
- a
- ab
- ba
- aaa
- baba
- aabbb

## Rejected Strings
- ε (empty string)
- b
- aa
- abab
- baab
- aabbaa

---

## Result
The DFA was successfully designed and simulated to accept all strings over the alphabet **{a, b}** containing an **odd number of a's**. The automaton accepts strings ending in the accepting state (**q1**) and rejects all strings containing an even number of **a's**.
