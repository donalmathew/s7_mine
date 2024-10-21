You're right. Let me teach more systematically following the exact syllabus.

1. LOGICAL AGENTS

1.1 Knowledge-Based Agents
- 
1.2 Logic



1.4 Propositional Theorem Proving

1.5 Agents Based on Propositional Logic
Example agent:
```python
class PropositionalLogicAgent:
    def __init__(self):
        self.KB = set()
    
    def update_KB(self, percept):
        # Convert percept to logical sentence
        sentence = self.make_percept_sentence(percept)
        self.TELL(sentence)
    
    def decide_action(self):
        # Query KB to find best action
        for action in possible_actions:
            if self.ASK(leads_to_goal(action)):
                return action
```

2. FIRST ORDER PREDICATE LOGIC (FOPL)

2.1 Syntax and Semantics of FOL
Syntax components:
- Constants: Objects (john, mary)
- Variables: Placeholders (x, y)
- Predicates: Relations/properties (Tall(x), Loves(x,y))
- Functions: Maps objects to objects (father_of(x))
- Quantifiers: 
  - ∀ (Universal: "for all")
  - ∃ (Existential: "there exists")

2.2 Using First Order Logic

2.3 Knowledge Representation in FOL
Techniques:
1. Categories and Objects
   ```
   Dog(fido)
   Cat(whiskers)
   ```

2. Properties and Relations
   ```
   Tall(john)
   Owns(mary, book)
   ```

3. Events and Time
   ```
   Happens(event, time)
   Before(time1, time2)
   ```

3. INFERENCE IN FIRST ORDER LOGIC

3.1 Propositional vs First Order Inference

3.2 Unification and Lifting
Unification algorithm:
```python
def unify(x, y, substitution):
    if substitution is None:
        return None
    elif x == y:
        return substitution
    elif is_variable(x):
        return unify_var(x, y, substitution)
    elif is_variable(y):
        return unify_var(y, x, substitution)
    # ... more cases
```

3.3 Forward Chaining

3.4 Backward Chaining
Algorithm:
1. Start with goal
2. Find rules that could prove goal
3. Recursively prove premises of these rules
4. Stop when reaching known facts

3.5 Resolution

Would you like to:
1. Practice problems with any of these topics?
2. See more detailed examples?
3. Focus on a specific area?