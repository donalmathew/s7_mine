![[Pasted image 20241020174119.png]]

Let me show you how to convert this First Order Logic sentence to CNF step by step.

1) First, let's write the English sentence in FOL:
   "Ravi likes all kind of food"
   Initial FOL: ∀x(Food(x) → Likes(Ravi, x))

2) Steps for CNF conversion:

   a) Eliminate implications (→):
   - Replace (P → Q) with (¬P ∨ Q)
   - ∀x(¬Food(x) ∨ Likes(Ravi, x))

   b) Move negations inward (not needed here as there are no negations to push in)

   c) Standardize variables (not needed here as we already have clear variable usage)

   d) Skolemization (not needed here as we don't have existential quantifiers)

   e) Drop universal quantifiers (implicit in CNF):
   - ¬Food(x) ∨ Likes(Ravi, x)

   f) Distribute AND over OR (not needed here as we don't have conjunctions)

Final CNF: ¬Food(x) ∨ Likes(Ravi, x)

The sentence is already in CNF because:
- It's a disjunction of literals
- All variables are implicitly universally quantified
- No implications remain
- No existential quantifiers exist
- No conjunctions need distribution

This is the simplest form of the sentence in CNF, representing "for every x, either x is not food OR Ravi likes x".


- another example:
### Example: Converting FOL to CNF

#### **Statement in Natural Language**:
"All humans are mortal, and there exists someone who loves all humans."

---

### **Step 1: Translate into FOL**
1. **"All humans are mortal"**:  
   \[
   ∀x (Human(x) → Mortal(x))
   \]  
2. **"There exists someone who loves all humans"**:  
   \[
   ∃y ∀z (Human(z) → Loves(y, z))
   \]  
   Combined FOL:  
   \[
   ∀x (Human(x) → Mortal(x)) ∧ ∃y ∀z (Human(z) → Loves(y, z))
   \]

---

### **Step 2: Eliminate Implications**
1. **"Human(x) → Mortal(x)"** becomes:  
   \[
   ¬Human(x) ∨ Mortal(x)
   \]  
2. **"Human(z) → Loves(y, z)"** becomes:  
   \[
   ¬Human(z) ∨ Loves(y, z)
   \]  
   Updated FOL:  
   \[
   ∀x (¬Human(x) ∨ Mortal(x)) ∧ ∃y ∀z (¬Human(z) ∨ Loves(y, z))
   \]

---

### **Step 3: Move `¬` Inwards (De Morgan’s Laws)**
- No changes needed here since negations are already in the simplest form.

---

### **Step 4: Standardize Variables**
- Rename bound variables in different quantifiers to avoid conflicts:
   - For the first quantifier: \(x\) remains \(x\).  
   - For the second quantifier: \(z\) is replaced with \(w\).  
   Updated FOL:  
   \[
   ∀x (¬Human(x) ∨ Mortal(x)) ∧ ∃y ∀w (¬Human(w) ∨ Loves(y, w))
   \]

---

### **Step 5: Skolemization**
- Remove existential quantifiers by introducing Skolem functions/constants:
  - Replace \(∃y\) with a Skolem constant \(c\), since \(y\) does not depend on any universal quantifiers.  
  Updated FOL:  
  \[
  ∀x (¬Human(x) ∨ Mortal(x)) ∧ ∀w (¬Human(w) ∨ Loves(c, w))
  \]

---

### **Step 6: Flatten into CNF**
1. Break the conjunction into separate clauses:
   \[
   (¬Human(x) ∨ Mortal(x))  
   \]
   \[
   (¬Human(w) ∨ Loves(c, w))
   \]
2. Generalize \(x\) and \(w\) into variables for CNF representation:
   - First clause: \(¬Human(A) ∨ Mortal(A)\).  
   - Second clause: \(¬Human(B) ∨ Loves(c, B)\).

---

### **Final CNF Form**:
\[
(¬Human(A) ∨ Mortal(A)) ∧ (¬Human(B) ∨ Loves(c, B))
\]

---

### Explanation of Key Steps:
1. **Eliminated Implications**: Converted "if" statements to logical disjunctions.  
2. **Standardized Variables**: Ensured unique quantifier variables.  
3. **Skolemization**: Introduced a constant \(c\) for the existential quantifier \(∃y\).  
4. **Flattened into CNF**: Converted the logical formula into a conjunction of disjunctions.

This example covers every aspect needed for the exam. Would you like further clarification or practice problems?