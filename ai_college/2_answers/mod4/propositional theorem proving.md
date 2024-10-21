This involves determining whether a statement is true based on a set of known facts using rules of inference:

Common rules:
1. Modus Ponens: 
   ```
   If P → Q is true, and P is true, then Q is true
   Example:
   P → Q: If it rains, the ground gets wet
   P: It is raining
   ∴ Q: The ground is wet
   ```

2. Modus Tollens:
   ```
   If P → Q is true, and Q is false, then P must be false
   ```

Methods:
1. Truth Tables
2. Inference Rules:
   - Modus Ponens: (P→Q, P) ⊢ Q
   - Modus Tollens: (P→Q, ¬Q) ⊢ ¬P
   - AND-Elimination: (P∧Q) ⊢ P
   - AND-Introduction: P, Q ⊢ (P∧Q)
   - OR-Introduction: P ⊢ (P∨Q)
   - Resolution: (P∨Q, ¬Q∨R) ⊢ (P∨R)
