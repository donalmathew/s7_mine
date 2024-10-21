- Starts with a goal
- Works backwards to find facts that would prove it
- Common in Prolog programming

Example:
```
Goal: Animal(Fido)
Rule: ∀x(Dog(x) → Animal(x))
Fact: Dog(Fido)

Backward chaining:
1. To prove Animal(Fido)
2. Look for rules with Animal in conclusion
3. Find: Dog(x) → Animal(x)
4. New goal: Prove Dog(Fido)
5. Find fact: Dog(Fido)
6. Therefore: Animal(Fido) is proven
```
