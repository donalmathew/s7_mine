![[Pasted image 20241021104750.png]]


Unification is finding substitutions that make different logical expressions identical.

Example:
```
Expression 1: Loves(John, x)
Expression 2: Loves(y, Mary)
Unification: {y/John, x/Mary}
Result: Loves(John, Mary)
```
example 2:
	![[Pasted image 20241021110312.png | 400]]

- Conditions for unification:
	1. Predicate symbols of the sentences must be same.
	2. Number of arguments in the sentences must be identical 
	3. Unification fails: Presence of two similar variables in the expression.

- example 3:
	![[Pasted image 20241021104750.png]]
	Let me solve this unification problem step by step.

	1) We have two expressions:
	   - Knows(Father(y), y)
	   - Knows(John, x)

	1) For these to unify, their predicates must match (they do - both are "Knows") and their arguments must unify.

	1) Let's look at the arguments:
	   First argument: Father(y) needs to unify with John
	   Second argument: y needs to unify with x

	1) Father(y) cannot unify with John because:
	   - John is a constant
	   - Father(y) is a compound term
	   - You cannot unify a constant with a compound term

	1) Therefore, NO UNIFIER EXISTS for these expressions.

	The reason is that there's no way to make Father(y) equal to John through any substitution of variables. Function terms (like Father(y)) and constants (like John) are fundamentally different and cannot be unified.

	If we were to write this formally:
	θ = NO UNIFIER (or null/failure)

	This is similar to trying to solve the equation Father(y) = John, which has no solution because they are structurally different terms.