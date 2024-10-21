- Starts with known facts
- Applies rules to derive new facts
- Continues until goal is reached or no new facts can be derived

Example:
```
Facts:
Dog(Fido)
∀x(Dog(x) → Animal(x))

Forward chaining:
1. Start with Dog(Fido)
2. Apply rule: If Dog(x) then Animal(x)
3. Derive: Animal(Fido)
```

Algorithm:
1. Start with known facts
2. Apply rules to derive new facts
3. Add new facts to KB
4. Repeat until no new facts can be derived
