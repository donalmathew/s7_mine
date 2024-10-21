Resolution rule:
```
From: P ∨ Q and ¬P ∨ R
Derive: Q ∨ R
```

Resolution algorithm:
1. Convert to Conjunctive Normal Form (CNF)
2. Apply resolution rule repeatedly
3. If empty clause derived, original statement is unsatisfiable
