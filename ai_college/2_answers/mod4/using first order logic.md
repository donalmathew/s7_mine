Common patterns:
```
// Facts
Student(john)
Teaches(prof, math)

// Rules
∀x(Student(x) → Person(x))
∀x∀y(Teaches(x,y) → Expert(x,y))

// Complex statements
∀x(Student(x) ∧ Studies(x) → WillPass(x))
```
